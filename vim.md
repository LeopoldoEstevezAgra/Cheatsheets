# *Vim cheatsheet*

**Note** : It is taken for granted that all of this command are run as without 
the use of the vim command line entering the ':' key and represented as a code 
block `command` .

**Note** : In case that the command is a ':'  command is going to be indicated 
presented between square brackets     `[...]`

**Note** : All elements within `{...}` are always command variables or something 
that the user must type 

**Note** : This cheatsheet is not only going to contain basic vim comands , some
of them are going to be from plugins or my own modification and remapings so some
of them may not work in your specific situation , checking my 
[dotfiles](https://github.com/LeopoldoEstevezAgra/dotfiles) in any doubt

**Note** : This cheatsheet represent my most used commands , some others that I
do not use may not be listed here, if you want to check a full list I recommend 
going to the official vim documentation

## Basic vim commands

### Movement commands

#### General cursor movements 

`k` : Move cursor up

`j` : Move cursor down 

`h` : Move cursor left 

`l` : Move cursor right 

`H` : Move cursor to top of the screen 

`M` : Move cursor to middle of the screen 

`L` : Move cursor to bottom of the screen 

`w` : Move cursor foward to start of a word taking in count puctuation

`W` : Move cursor foward to start of a word without taking in count punctuation

`e` : Move cursor foward to end of a word taking in count puctuation

`E` : Move cursor foward to end of a word without taking in count punctuation

`b` : Move cursor backwards to start of a word taking in count puctuation

`B` : Move cursor foward to beggining of a word without taking in count punctuation

`%` : Jumps to the maching `{} () []`

`0` : Jumps to the very start of a line ignoring tabs or spaces

`^` : Jumps to the first non blank character of the line  

`$` : Jumps to the very end of a line ignoring tabs or spaces

`g_`: Jumps to the last non blank character of the line  

`gg`: Jumps to first line of the file 

`G`: Jumps to the last line of the file

`{number}G``{number}gg` : Jumps to specified line in the document

#### Character finding 

`f{character}` : Jumps to the next ocurrence of the specified character

`t{character}` : Jumps to the previous ocurrence of the specified character

`,` : Repeats last f or t command backwards

`;` : Repeats last f or t command fowards 

#### Camera control 

`zz`:  Centers the camera over current cursor position

`zt`:  Sets the camera and cursor on the top of the screen

`zb`:  Sets the camera and cursor on the bottom of the screen

`<ctrl>e`: Move the escreen one line down without moving the cursor

`<ctrl>y`: Move the escreen one line up without moving the cursor

`<ctrl>b`: Moves the camera back one full screen 

`<ctrl>f`: Moves the camera fowards one full screen 

`<ctrl>d`: Moves the camera back half screen 

`<ctrl>u`: Moves the camera fowards half screen 

## Editing commands

#### Insert mode 

`i`: Enters insert mode before the cursor position 

`I`: Enters insert mode at the beginning of the line 

`a`: Enters insert mode after the cursor position 

`A`: Enters insert mode at the end of the line 

`o`: Enters insert mode in a new line below the current cursor line

`O`: Enters insert mode in a new line above the current cursor line

`<esc> or jj`: Exits insert mode 

#### Command mode 

`{command} i {movement}` : Apply that command to the 'inner' or 'selected' element

`u` : Undo last command

`.` : If last command is repeatable, repeat it 
##### Editing

`r`: Replaces the character under the cursor 

`c{movement}`: Deletes the selected element and enters insert mode 

`>>`: Adds one tab foward to the block

`<<`: Removes one tab to the block

`~`: Switch case

##### Cut, copy, paste

`yy`: Copies line

`y{movement}`: Copies block or segment present on that movement 

`dd` : Deletes line

`d{movement}`: Deletes block or segment present on that movement 

`p`: Pastes content from clipboard after the cursor

`P`: Pastes content from clipboard before the cursor

`x`: Deletes a single character

##### Searching

`/{pattern}` : Search patern forward

`?{pattern}` : Search patern backwards

`n` : Repeat search in the same direction

`N` : Repeat search in the oposite direction

##### Window management

`<ctrl> w {direcction}` : Jumps to window in that given direction

`<ctrl> w {Uppercase direcction}` : Rotates windows in that direction 

`<ctrl> ws` : Splits a window horizontally 

`<ctrl> wv` : Splits a window vertically

`<ctrl> ww` : Switch windows positions

`:q` : Closes the current window

`:qa` : Closes all tabs

`:q!` : Closes the current window without saving changes

`:w` : Saves the current windows changes

`:wq` : Closes the current window saving the current changes

##### Tabs management

`:tabnew {optional file}` : Opens a new tab

`:tabc` : Closes current tab and all its open files

`:tabmove {position}` : Moves the current tab to the given th index

`:tabo` : Closes all tabs except the current one

`{optional index} gt` : Jumps to next tab (if given jumps to specified index)

#### Visual 

Same commands as in normal mode

`v` : Enters visual selection mode

## Plugings 

#### NerdTree

**Note**: In order to move in the tree itself normal vim movement keys are used

`<ctrl>m` : While not in nerdtree open a close the tree window

`?` : While on nerdtree to open a help menu

##### Directory control

`o` : Opens and closes the directory where the cursor is placed, in case that is 
a file instead of a directory that will open said file in the last editor window
used

`x` : Closes the current folder node 

`p` : Go to parent node 

`P` : Go to root node

`C` : Change root to selected directory

`R` : Refresh root directory

`I` : Show all hidden files

##### Creating and renaming files

`m` : Opens contextual menu that allows you to rename, delete etc files

##### Opening files

`o` : Open file in the last editor window used

`s` : Open file in a new vertical split

`i` : Open a file in a new horizontal split

`t` : Open file in a new tab

`T` : Open a file in a new tab without jumping to it
