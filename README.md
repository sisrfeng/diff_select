# spotdiff.vim

##A range selectable diffthis

### Introduction

This plugin has been developed in order to make diff mode more useful.
Vim always makes a diff for all lines in a window. But this plugin allows
to specify the range and then partially make a spot diff.

This plugin provides another `:diffthis` and `:diffoff` commands, which are
`:Diffthis` and `:Diffoff`.

You can use `:Diffthis` to select a block of lines and to make the current
window diff mode. Selected lines are visually color-marked at line head.
When two separate windows become diff mode, `:Diffthis` shows their spot diffs
in those windows without opening a new window and tab page.

Use `:Diffoff` to clear the selected block of lines and to reset diff mode
for the current window. If `!` is specified, clear and reset for all windows
in the current tab page.

This plugin also makes it possible to select two blocks of lines in a single
window, to see the differences between them within one file. `:Diffthis` tries
to open a temporary new window above or below of the current one, copies
secondly selected lines to it, and makes spot diffs with source window.
This temporary window will be closed when `:Diffoff` is used on it.

Please do not use the original `:diffthis` and `:diffoff` together with
`:Diffthis` and `:Diffoff` to prevent any errors and troubles. Try `:Diffoff!`
to reset all in the case.

It is recommended to install **diffchar.vim** plugin
(https://github.com/rickhowe/diffchar.vim) so that
you can see the exact differences.

### Command

* `:[range]Diffthis`
  * Select a block of lines with `[range]` and to make the current window
    diff mode. If `[range]` is not specified, the current line will be
    selected. It is possible to select two blocks of lines in a single
    window to see the differences between them.

* `:Diffoff[!]`
  * Clear the selected block of lines and reset diff mode for the current
    window. If `!` is specified, clear and reset for all windows in the
    current tab page.

### Demo

![demo](demo.gif)

In this demo, the **diffchar.vim** plugin has been installed.
