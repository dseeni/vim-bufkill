# vim-bufkill

In Vim, trying to unload, delete or wipe a buffer without closing the window or split? You'll like this:

**With bufkill:**

![With bufkill](http://i59.tinypic.com/2mh6kc6.gif)

**Without bufkill (standard Vim behaviour):**

![Without bufkill](http://i58.tinypic.com/jaweg6.gif)

The inspiration for this script came from:
 * My own frustration with vim's lack of this functionality
 * The description of the emacs kill-buffer command in tip #622 (this script basically duplicates this command I believe, not sure about the undo functionality)
 * Comments by Keith Roberts when the issue was raised in the vim@vim.org mailing list.

*Note: This is the official Git repo which replaces http://www.vim.org/scripts/script.php?script_id=1147*

## Installation

This plugin follows the standard runtime path structure, and as such it can be installed with a variety of plugin managers:

  * [Pathogen][1]
    * `git clone https://github.com/qpkorr/vim-bufkill ~/.vim/bundle/vim-bufkill`

  * [Vundle][2]:
    * `Plugin 'bling/vim-airline'`

## Usage

#### Unloading/Deleting/Wiping

When you wish to unload a file from the buffer and keep the window/split intact:

`:BUN`

When you wish to delete a file from the buffer and keep the window/split intact:

`:BD`

When you wish to wipe a file from the buffer and keep the window/split intact:

`:BW`

Notice how the key mappings are the uppercase version of the `:bun` `:bd` `:bw` Vim commands? Easy!

#### Moving through buffers

To move backwards through recently accessed buffers:

`:BB`

and to move forwards:

`:BF`

To move to an alternate buffer and keep the cursor in the same column, use:

`:BA`

#### Also...

You can also override `Ctrl-^` (Vim's default for swapping between alternate buffers) via `g:BufKillOverrideCtrlCaret` in your `/.vimrc` file.

You can overide the default mappings within your `/.vimrc` file like so:

`map <C-c> :BD<cr>`

resulting in being able to delete a file from the buffer via vim-bufkill with <kbd>CTRL</kbd> + <kbd>c</kbd>

## Contributions

Contributions and pull requests are welcome.

[1]: https://github.com/tpope/vim-pathogen
[2]: https://github.com/gmarik/vundle
