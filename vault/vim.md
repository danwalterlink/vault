---
id: ofqbpuijaf1ev0hh54rudts
title: Vim
desc: ''
updated: 1685985444658
created: 1636203835676
---

goTo last non-whitespace char?

## keyboard layout implications
qwerty - qwertz : remap yank to z #?

closing vim #p ZZ
## bindings
 --> international
 - [ ] backtick-mark traversal is broken
 - [ ]
 ---

base building block
- buffer

matching character = %
matching under cursor */#

#research
next group : }
## goto next/previous mark
[how to move to the next enclosing brackets in VI](https://stackoverflow.com/questions/1509855/how-to-move-to-the-next-enclosing-brackets-in-vi)

use [ and ] to cycle to the previous and next matching brackets respectively. Commonly:

[( - Previous (
[{ - Previous {
[< - Previous <
and more interesting ones

[m - Previous method start
[M - Previous method end
The same also applies for next items:
]} - Next }
]) - Next )
]> - Next >
The reason why this method is more effective is that you can specify count together with the commands

## motions
f, t are direction-specific
: sneak remapping s to extended f
$ goes to last character in line
g_ : last non-blank character

## marks
delete all with :delmarks!
issues with global marks

list global marks:
:marks

## substitute
\%V constrains to visual selection
:s/\%Vsearch/replace/mod

#q how to regex in ":s//g"?

# selection
gv : ![[Task|dendron://task/task]]ct last visual selection

## surround - [vim.surround](https://github.com/tpope/vim-surround)
:v S(surroundings)
  for brackets/braces, closing braces insert without spaces
:n
  ys(move)(surroundings)
  cs(move)(surroundings)

### brackets
ysi(Bracket)
  [ with space
  ] without

### selection
S and the same commands as before

## search case sensitive
:set smartcase/ignorecase/noignorecase

## remove highlighting
:noh // user.binding: C-n

## reselect visual
* gv
#? paste to eol?
## insert to [motion]
move to space in normal
get to insert
^r and specify register to paste

#? how to navigate filetrees?
-> :e . netrw in current dir, but navigation breaks

## literal input
C-v in input mode and enter character
-> escape sequences

## merge [Merge changes using vimdiff](https://stackoverflow.com/questions/27832630/merge-changes-using-vimdiff#answers)
-> [[vim.plugins#fugitive]]
do - Get changes from other window into the current window.
dp - Put the changes from current window into the other window.
]c - Jump to the next change.
[c - Jump to the previous change.
zo - Open folded lines.
zc - Close folded lines.
zr - Unfold both files completely.
zm - Fold both files completely.
Ctrlww - change window.
:only | wq - quit other windows, write and quit
Quirks to watch for

Both do and dp work if you are on a block of change (or just one line under a single line of change) in Normal mode, but not in Visual mode.
The undo command will only work in the buffer that was changed, so if you use dp and change your mind, you need to switch to the other buffer to undo.
:diffupdate will re-scan the files for changes (Vim can get confused, and show bogus stuff).
Visual mode and finer grained control

When selecting lines of text in Visual mode, you must use the normal commands:

:'<,'>diffget and
:'<,'>diffput.
For example:

Enter Visual mode and mark some text/lines.
Then type :diffput to push the selected lines to the other file or :diffget to get the selected lines from the other file.
To belabor the point: This means that if there is a block of changes consisting of multiple lines, then selecting a subset of lines and issueing :diffput will only apply those changes in the other buffer.

(:diffget and :diffput also accept ranges, see :h copy-diffs for more.)

Compare two buffers inside Vim

If you load up two files in splits (:vs or :sp), you can do :diffthis on each window and achieve a diff of files that were already loaded in buffers.

:diffoff can be used to turn off the diff mode.

This Vimcasts post and video show this in practice.

How to apply all changes between buffers

Make sure that all participating buffers are in diff mode (see :h start-vimdiff)
a. Get changes from a buffer to the current one: :%diffget <buffer-number>
b. Put all changes from current buffer into another: :%diffput <buffer-number>
(:% is a range to select the entire file; see :h :%. :ls will show currently opened buffers.)