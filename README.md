## Setup Environment

Install neovim locally is necessary
```
$ mkdir -p "$HOME/.local/bin"
$ curl -fLo "$HOME/.local/bin/nvim" https://github.com/neovim/neovim/releases/download/stable/nvim.appimage
$ (sudo) chmod u+x "$HOME/.local/bin/nvim"
```

copy file https://raw.githubusercontent.com/fanyun-sun/pika-vim/master/init.vim to `.config/nvim/init.vim`


## General cheat sheet
* Terminal: Ctrl-A/Ctrl-E for Home/End
* vimperator: zZ ==> reset zoom

## Tmux cheat sheet
* ```<Prefix> &``` for killing a window
* ```<Prefix> x``` for killing a pane
* ```<Prefix>(hold) arrowKey``` for resizing pane

## Vim cheat sheet

* copy/paste among tmux panes running vim instances
```
" copy to buffer
vmap <C-b> :w! ~/.vimbuffer<CR>
nmap <C-b> :.w! ~/.vimbuffer<CR>
" paste from buffer
map <C-m> :r ~/.vimbuffer<CR>
```

* Plugin
	* [repmo.vim](https://github.com/vim-scripts/repmo.vim)
	* [taglist.vim](https://github.com/vim-scripts/taglist.vim)

* . ==> repeat last change in normal mode
* Ctrl-^ to edit the alternate-file
* same command on contiguous lines
	1. Select the lines you want to modify using Ctrl-v.
	2. Press:
	    * I: Insert before what's selected.
	    * A: Append after what's selected.
	    * c: Replace what's selected.
	3. Type the new text.
	4. Press Esc to apply the changes to all selected lines.

* You can use it with the d command, to delete all lines that contain a particular pattern, or all lines that do not contain a pattern. 
	* For example, to delete all lines containing "profile" (remove the /d to show the lines that the command will delete):
	<br>**$ :g/profile/d**
	* More complex patterns can be used, such as deleting all lines that are empty or that contain only whitespace:
	<br>**$ :g/^\s*$/d**


* The command to repeat an f is ; (semicolon) <br> , (comma) reverses the direction of the search.

* Use the normal command in Ex mode to execute the macro on multiple/all lines:

	Execute the macro stored in register a on lines 5 through 10.<br>
	**:5,10norm! @a**

	Execute the macro stored in register a on lines 5 through the end of the file.<br>
	**:5,$norm! @a**

	Execute the macro stored in register a on all lines.<br>
	**:%norm! @a**
	
	Execute the macro store in register a on all lines matching pattern.<br>
	**:g/pattern/norm! @a**

* vim copy visual mode seletected text to system clipboard 

	https://askubuntu.com/questions/613170/vim-and-system-clipboard
	
	"+y to yank, Ctrl-Shift-v to paste
* **:set list** to disply invisible characters
