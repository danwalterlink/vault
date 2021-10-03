---
id: u5a2r3t5crdr76nrndm3h1h
title: Vim
desc: ''
updated: 1677757558308
created: 1636203835676
---
closing vim #p ZZ
## bindings
 --> international
 - [ ] backtick-mark traversal is broken
 - [ ]
 ---

base building block
- buffer

matching character = %

#research
next group
}

## motions
f, t are direction-specific

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
gv : reselect last visual selection

## surround - vim.surround
:v S(surroundings)
  for brackets/braces, closing braces insert without spaces
:n
  ys(move)(surroundings)
  cs(move)(surroundings)

### brackets
ysi(Bracket)
  [ with space
  ] without

## search case sensitive
:set smartcase/ignorecase/noignorecase

## remove highlighting
:noh

## reselect visual
* gv
for surround commands, now that we have brackets, the ys-commands work

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