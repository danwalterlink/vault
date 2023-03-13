---
id: 38v7lg418kuf6s7db3gc2ea
title: Lens
desc: ''
updated: 1633199319649
created: 1633199319649
---

# Essentially, they represent the act of “peering into” or “focusing in on” some particular piece/path of a complex data object such that you can more precisely target particular operations without losing the *context* or structure of the overall data you’re working with.

There are already several great libraries out there for working with Lenses in Javascript: in particular, check out [Brian Lonsdorf’s lenses](https://github.com/DrBoolean/lenses) (which use [fantasy-land](https://github.com/fantasyland/fantasy-identities) functionality and [point-free wrappers](https://github.com/DrBoolean/pointfree-fantasy), and are not to be confused with Brian McKenna’s [fantasy-lenses](https://github.com/fantasyland/fantasy-lenses)) and [Ramda](http://ramdajs.com/), a functional library which provides a bunch of powerful Lens methods. So if you just want to start using Lenses, great: there they are!

But at least when *I* first came across them, I wanted to dig into how they *really* work, how I’d build them myself, etc. And there, things were a little bit harder.

Most of the articles on Lenses are [written for users of Haskell](https://www.schoolofhaskell.com/user/tel/lenses-from-scratch) (where they solve a larger set of language problems less relevant to Javascript). I couldn’t find much discussion of them targeted at Javascript users like myself. Lonsdorf does have a [pretty great video on the topic that answered most of my questions](https://vimeo.com/104807358), but a video isn’t an article, and I still needed to work through things on my own.

So, with the caveat that I’m not a mathematician, Haskell-er, or an expert by any means, here’s my bit-by-bit walkthrough of a (mostly) stand-alone implementation in schwifty ES6 syntax. Hopefully, by following along, I can help you avoid blind-alleys in your own exploration of the concept.

So. As I said, what was neat about ***lensOver*** is that it allowed us to very succinctly target a *particular* function at a *particular* part of a complex data object, and yet still get back the entire (cloned and updated) object. This allowed us to just chain together a bunch of pure, declarative operations like, say, mapping over arrays… and just apply some simple functions that we already had handy instead of breaking down and writing long-winded, imperative solutions.

Without worrying too much about the exact form of the ***lensOver***/***map***/***capitalizeFirst*** functions, that means we can do things like this:

That is, we create a construct that focuses in on the “comments” node of an object, maps over that array by next focusing in on the “body” node of each inner object and applying a simple function to it. Finally, it gives us back (a copy of) the *entire* (now updated) data object instead of just the part we worked on. At that point, we could just run the function with some data (bigBird) and see the result, as above. Or we could hold off specifying what data to work over and get back a partially applied ***lensOver*** operation that we could assign to a variable, pass around, compose into a larger program, etc.

One other really important thing to note is that ***lensOver*** here is acting a *lot* like a generic ***map*** operation: it takes some container (just like an Array of [1,2,3,4] is a container of sorts) opens it up, does stuff to it, but then finally returns the same *sort* of container back to us; something with the same structure we started with. We could, of course, alter the structure at and below the node that the Lens was focusing on, but not anything higher up.

I hope you think that’s a pretty cool pattern, but the implementation there was written as a kludgy one-off (and I won’t even cover how it worked, since we’re about to improve on it). It was at once both overloaded (doing too much in one go) and brittle.

The only thing that even marginally justified using “lens” in the name is that it, at least externally, seemed to do something that is central to what Lenses do: combine getting and setting particular values into a single operation (just an overly verbose, inelegant imperative one).

Without getting into ***lensOver***’s structure, it should be obvious that running a function like ***capitalizeFirst*** on a deeply nested value must necessarily both *get* that specific value from the existing object, plug what it finds some transforming function as its input, and then swap out the old value for the *result* of that function, thus *setting* it to the new one.

Real Lenses will generalize exactly that combined “getting and setting” idea.

Before we walk through building a real Lens implementation though, let’s talk about the functional toolset we’re going to need: [composing](https://medium.com/@dtipson/creating-an-es6ish-compose-in-javascript-ac580b95104a#.4sbls78zn), [currying](http://ramdajs.com/docs/#curry), [mapping](http://ramdajs.com/docs/#map), array and object cloning AND splicing, the [K Combinator](http://ramdajs.com/docs/#always) and, finally, slightly cannibalized bits of the Constant and Identity Functors.

Let’s start with the 1st three.

Compose is just the ES6 version of a [variadic compose I worked through here](https://medium.com/@dtipson/creating-an-es6ish-compose-in-javascript-ac580b95104a#.4sbls78zn).

My quick-n-dirty version of ***curry*** here is really sort of an “autocurry”: that is, it takes a function with a set/known number of arguments and then allows us to call that function with the arguments grouped in any which way we want. ***(1,2,3)*** or ***(1,2)(3)***, or ***(1)(2)(3)***: whatever. If the total number of arguments passed so far isn’t enough, it just returns a new, partially-applied function waiting for the remaining arguments.

***mapWith***, finally, is just a curried, “point-free” version of a map operation, meaning that we can pass it the function first and then later pass it the Functor (a “mappable”) that we want to map over before getting a result. It’s important that ***mapWith*** delegates the ***.map*** operation to the Functor itself, meaning that it knows nothing about how the Functor interprets what “mapping” is (other than it obeys the Functor Laws).

These are all useful tools in their own right, and you can find them in most functional libraries. But it’s worth seeing and thinking through how they’re constructed: how they do what they do.

Next we’ll look at the least interesting bits: the direct setting and getting functions:

Heh, well: so, cloning arrays and objects is tricky business. I have my own implementations written out, but it’s not really worth the time to talk through them, so we’ll just use Ramda’s versions (exactly as they do with their own Lens implementations). Ideally, the splicing/setting functions will take three arguments in this order: first a reference to *where* to splice/set, then the new value, and finally the actual object or array to transform. Ideally, they’d also properly clone the object/array, which is something we’re not going to worry about explaining too much for now, thanks to Ramda. Let’s move on to the good part: the actual Lenses!

Yep: getting and setting are fundamentally being expressed as, well… a single ***map*** operation. The setting part (the function that’s going to be applied to some [Functor](https://jcouyang.gitbooks.io/functional-javascript/content/en/functor_&_monad/functor.html)) is on the left, and the getting part (the thing we’re running the map operation *on*) is on the right.

Note also that the getter is wrapped *inside* the function ***f*** that we’re passing into the lens, which is not quite what it seems. That function is NOT, at least not directly, the transforming function that, say, the Lens ***over*** operation will ultimately use to update the value.

More on that soon, but first, something else should strike you as weird about all this. As we saw from ***lensOver***, these setting/getting operations will sometimes be applied to, well, things like strings and numbers. What does it even mean to “map” over a number? Or a string? It *is* weird, right? But it’s also a powerful abstraction, and when we actually *do* things with these lenses, we’ll see how this seeming oddity is overcome.

Let’s look at the final set of toolset functions for a hint at what’s going to happen:

Now this is all very suspicious. We know that Lenses are going to rely, heavily, on calling the setter/getter “***mapWith***” method on… well, something, and you might have assumed that it was going to be something familiar like an Array that actually HAS a native ***.map()*** method. But if that was really all “mapping” over something meant… then we wouldn’t have a special word like Functor in the first place: we’d just talk about Lists or Arrays and be done with it.

But “mapping” has a much broader meaning than just applying a function to each item in an ordered list. Again: “Mapping” over something in a larger sense means taking a particular *type* of “container” (of which an array of values is just one kind), opening it up, applying a function to the contents in a way that’s in accordance with the logic of that container, and then returning the same *type* of container, structurally intact.

From this, we can intuit that primitive values probably aren’t going to be worked on directly (they don’t *have* ***.map()*** methods after all!): they’re instead going to be wrapped in *some* sort of special container that does. So here, finally, are the core Lens *operations* & how they make exactly that happen:

Let’s unwrap (heh) what’s going on here. We know that the core Lens methods are, themselves, curried. That means that we can call ***objectLens*** with just the first argument (the key/index) and get back a new function waiting for more arguments.

Well, that first new, partially-applied function actually *is* the Lens for that particular key or index: you can think of it as storing a reference to the location of some piece of data: it’s an instruction about where to look (without yet having to specify what we’ll be looking *at*). And it’s *that* (the first step of ***arrayLens***/***objectLens***)which we’re going to pass into ***view***/***set***/***over*** as the first “*lens*” argument.

Heck, instead of ***arrayLens***/***objectLens***, we probably could have called those functions ***executeArrayLens*** or ***executeObjectLens***, because once they have all 3 of their arguments, they’re really *executing* some lens-related behavior, not just *defining* the Lens. ***view***/***set***/***over***, then, are helpers that complete the execution of ***arrayLens***/***objectLens*** by passing it the rest of its arguments in a particular way.

Those 3 different execution operations require further explanation:

***View*** is the simplest case: it’s all about just extracting and returning the property found at a particular location (a very similar in result to a lodash-fp _.get). We’re simply passing in a Lens and then, later, the target object/array that we want it to work on.

What is ***view*** actually *doing* with those two elements? As we said: it’ll be filling in the remaining arguments to the lens function. So the function ***f*** that the lens function actually gets is… the constructor for the Functor, ***Const***. Because of how ***Const*** is structured, that means that when the getter portion of the Lens runs ***Const*** on the retrieved value, it’ll return a ***Const*** Functor with the retrieved value now stored in the property, “value.” But ***Const*** also has its own special “map” operation defined, which means that when the ***arrayLens***/***objectLens*** runs ***mapWith***, it’ll use ***Const****’s* particular implementation of ***.map***. And what does *that* version of map do with the function passed into it?

Well, its signature this: ***map() => return this;*** so…

(image/jpeg)

Yep, it ignores it completely: that nullary signature doesn’t take or use *any* of the arguments passed to it, which means that it’ll just ignore the setter operation entirely. ***Const*** is instead built to just return the same exact ***Const*** whenever it’s mapped over: the one that already contains theresult of the getter. Which means we can then finally access and return it with [‘value’]. Done.

If that all seems like a *heck* of a lot of work just to access a property, ok. True. But ***view*** is just one simple operation in a toolkit. If you don’t find it particularly exciting, then lets take a look at the star-player, ***over***.

***over*** is going to play a similar trick as ***view*** did, in that what we’re *actually* having the lens map over is the Functor, ***Identity***.

Now things get a bit more convoluted. The function passed into the lens retrieves the value of the getter and returns an ***Identity*** Functor with *its* value property set to the *result* of the outer function we wanted to apply. This whole construct is then passed to the setter. The setter runs the map method of the ***Identity*** construct, which returns *another* ***Identity*** Functor that has *its* value property set to the result of running the *setter* function using the already altered value as the “replacement.” The resulting value is a copy of the entire object + one modification.

Because this whole process involves *two* calls of ***Identity(f(x))***, it might look like the focused-on value is going to get altered twice. But while the first ***Identity(f(x))*** is indeed transforming the value, the second is actually transforming the entire object/array (hence my attempt to name the arguments ***apf*** in one case, and ***mapf*** in another). What looks convoluted and repetitious is actually pretty elegant and parsimonious: it’s re-using the same Identity construct to do two different things (both necessary to attain the correct final result).

That just leaves the ***set*** operation. After the first two, it’s pretty simple: it’s just a special case of ***over*** that happens to bake-in a *particular* function to pass to ***over***: ***_K***.

That’s just the ***K*** combinator ( ***x => () => x*** )! Which is to say, it’s a function that returns *another* function that, regardless of what arguments *it* gets, *always* returns the original argument it got from the first step. That means that the transforming function passed to the getter (and then to the setter) will always just spit out the originally specified value, totally ignoring the getter value.

Interestingly, all three of these methods basically work by hijacking the core getting/setting construct in different ways:

* the ***view*** operation bypasses the setter by returning a Functor construct with a map operation that turns the setter in a no-op
* the ***over*** operation also defines its own special meaning for map such that the same Functor construct (***Identity***) can transform both the focus of the Lens and return the complete updated object/array
* the ***set*** operation uses the ***K*** combinator to bypass the value of the getter when ***over*** performs its larger-scale transformation

Again, that might seem like a lot of extra work (since certain parts of the Lens don’t actually run or matter in various cases), but that’s not how I see it: a lot of mileage is made out of a basic, elegant setup.

If it’s not obvious why that’s all so useful, that’s probably because we haven’t really demonstrated how we can use Lenses yet.

In practice, you’ll find that Lenses have another killer feature, which is that they, themselves, compose. In the simplest form, that means that ***compose(objectLens(‘comments’), arrayLens(0))*** creates a Lens that’s focused on the path [“comments”][0] . Doing this leaves us with an ordered set of instructions: “go through the door marked ‘comments’, then the door marked 0.”

Lonsdorf’s Lenses include a utility called “***makeLenses***” which allows you to pass a list of string keys. The result (which he usually assigns to a variable name like L for convenience) is an object that contains all the pre-baked Lenses you might need in a particular program. Here’s a similar version in written variadic form that also uses the set Lens operation internally:

With the result of that ***makeLenses***, we’d have all the components we need to compose a Lens that peeks into a comments prop, then peeks into the *first* comment in that array, and then finally peeks into the body property of that first comment. And/or we can use/reuse the individual components for composing other complex foci. The set of instructions we assemble knows nothing about the data we’ll pass through it: it’s entirely abstract.

Ramda implements a [utility with a similar purpose: ***lensPath***](http://ramdajs.com/0.19.0/docs/#lensPath). It allows you to specify an entire path all in one go, as an array, which also might be useful. Again, here’s my quick variadic version, which basically assumes that strings are object props and numbers are array indices:

Note that there are all sorts of design decisions to make. The authors of Ramda, for very good reasons (like consistency with all their other methods), did *not* make their ***lensPath*** method variadic: it instead takes a single array, not the array spread out into an arbitrary number of arguments. With ES6 syntax, it’d be easy to “fix” up my version to work that way instead by doing this: ***const RlensPath = (arr) => lensPath(…arr)*** Or, we could improve my version a bit by implementing a flatten operation on at least the first argument (in case you pass it a single Array), allowing it to work both ways.

Or whatever: the point is still that the underlying utility here is that we can represent paths *as* arrays, which also happens to be how a lot of other data manipulation libraries ([baobab](https://github.com/Yomguithereal/baobab) for one) do it. Arrays are a good format for representing paths largely because they’re themselves easy to reason about and build up dynamically. And if you wanted to use the lodash way of string paths ‘comments.0.body’ you could just use ***str.split(.)*** on a string argument.

Here’s another neat thing we can do, which Lonsdorf talks about in his video and implements in his Lens library: ***mapped***. (Oy, we’re talking an awful lot about mapping here aren’t we?) My version looks like this (different from his largely because he’s creating and using slightly more robust versions of the core Functors than I am here):

***mapped*** is a particular sort of lens that knows how to run a map operation on a Functor: think of it as your set of instructions splitting up (“clone yourself and go through all the doors at once”) at that point. Since the Functors in the example usage above are Arrays within Arrays, we’ll actually want to compose together *two* map operations so that the target function is applied to the each of the inner items of each of the inner arrays. And that just works. Neat.

Note that we also could have used just one ***mapped*** Lens and then passed the ***over*** method a partially applied ***mapWith***:

That’s a little less intelligible, in my opinion, but it’s worth seeing how the same operations can be represented as Lenses, partially applied functions, etc. Now let’s look at an even more complex example. Say that we have a collection of objects, each with a property “id.” Unfortunately, the ids are coming from an api we don’t control… and it represents them all in string format while our runtime code expects them all to be integers. Boo. Well, we can use lenses to very concisely describe what we need to have happen:

Let’s also not forget that operations like ***set*** and ***over*** are themselves curried, which opens up a lot of flexibility when we partially apply them (i.e. maybe add in the function or value we want to apply or set, but still hold off on specifying which data structure the operation should run on so that we can reuse it):

Really powerful behavior… all built up from simple, intelligible components. Great, right? If you’re ready to play around with the complete set of Lens methods: [here’s a REPL with everything put together](http://goo.gl/qujV6l).

There’s even more to learn about Lenses than just this (e.g. all “well-behaved” Lens implementations should obey a [particular set of laws](https://www.schoolofhaskell.com/user/tel/lenses-from-scratch#laws), and there are even more complex operations possible, and there are [even other flavors of Lenses](https://www.schoolofhaskell.com/school/to-infinity-and-beyond/pick-of-the-week/a-little-lens-starter-tutorial), though I’m not sure how easily any of that translates into Javascript, etc.), but wrapping my head around all this was enough for today. Hopefully you’ll try wrapping some Lenses around your data soon!

Addendum (1/22): Just to prove that I don’t know what I’m talking about when I said I couldn’t find any good articles on Lenses, [Lonsdorf wrote an article about Lenses](https://medium.com/@drboolean/lenses-with-immutable-js-9bda85674780) (and getting the “Immutable” part right using Immutable.js) yesterday. It also includes a link to [this pretty great read on why Lenses are a superior solution to many imperative/refactoring challenges](http://joneshf.github.io/programming/2015/12/19/Lenses-and-Virtual-DOM-Support-Open-Closed.html) by Hardy Jones.

One thing the Lonsdorf article also made me realize that I should note is that, unlike Ramda, my quick little implementation isn’t directly exposing a way to quickly define a custom getter/setter pair for a Lens. Why would you want to do that? Because you might want to get/set on something other than native objects/arrays (Lonsdorf’s article is all about using Immutable.js collections, for instance). It’d be easy to add an additional abstraction level to things (a method for creating a lens by specifying a getter/setter and then just re-implementing our stock object/array Lenses with it), but it’s definitely worth mentioning, and in that spirit, here’s a quick re-write to add a higher-level way of defining a Lens:

…which allows us to re-implement our array and object Lenses as well as more easily define new Lens types that will work on a different structures, such as a [ES2015 Map](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map). We *could* have just written a one-line mapLens function with the ***.get()***/***.set()*** built in of course, but it’s almost always nicer to break things down into simple, composable parts.

Here’s [a new REPL so you can experiment](http://goo.gl/MpWnuV) with all that.

Next time: [Transducers](https://medium.com/@dtipson/everything-reduced-transducers-in-javascript-8ea3459bc7f9#.nowf75iv8).

— Medium: Drew Tip
