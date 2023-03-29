---
id: tgslwm8h0kupakddwut2gtl
title: Git
desc: ''
updated: 1680000198893
created: 1664713853433
---

## env
- sensible global config
  setting user vars
- automation
  commit templates
  hooks

## (cli)tools
- gitui
- tig

sparse checkout
  - init git
    set 'sparse-checkout' to pattern

## nested branch modules
if narrower branch A' of named master branch A:base
  then A' contains only diffs on A:base and needs rebaseing onto A:base to be feature-complete

## dotfile reo
- detached work-tree
- modified base functions:
  pull : rebase 'name:feature' onto master:master

![[Workflow|dendron://vault/dendron.workflow]]
