# Operators and motions

In `dw`:

- `d` is an operator, the delete operator
- `w` is an motion, is what the operator will operate on

Using a count for a motion

- Exampoe: type  2w  to move the cursor two words forward.

# Undo and redo

- Undo: `u`
- Redor: `CTRL-R`

# Moving the cursor around the file

- `gg`: go to the start of the file
- `G`: go to the end of the file
- `55 G`: number of the line and press `G`, go to that line

# The seach command

 1. In Normal mode type the  /  character.  Notice that it and the cursor
    appear at the bottom of the screen as with the  :	command.
 2. Now type 'errroor' <ENTER>.  This is the word you want to search for.
 3. To search for the same phrase again, simply type  n .
    To search for the same phrase in the opposite direction, type  N .
 4. To search for a phrase in the backward direction, use  ?  instead of  / .
 5. To go back to where you came from press  CTRL-O  (Keep Ctrl down while
    pressing the letter o).  Repeat to go back further.  CTRL-I goes forward.

# The substitute command

Type  :s/old/new/g  to substitute 'new' for 'old'.

 1. Move the cursor to the line below marked --->.

 2. Type  :s/thee/the <ENTER>  .  Note that this command only changes the
    first occurrence of "thee" in the line.

 3. Now type  :s/thee/the/g .  Adding the  g  flag means to substitute
    globally in the line, change all occurrences of "thee" in the line.

 4. To change every occurrence of a character string between two lines,
    type   :#,#s/old/new/g    where #,# are the line numbers of the range
                              of lines where the substitution is to be done.
    Type   :%s/old/new/g      to change every occurrence in the whole file.
    Type   :%s/old/new/gc     to find every occurrence in the whole file,
                              with a prompt whether to substitute or not.

# Executing an external command

Type  :! followed by an external command to execute that command.

 1. Type the familiar command 	:  to set the cursor at the bottom of the
    screen.  This allows you to enter a command-line command.
 2. Now type the  !  (exclamation point) character.  This allows you to
    execute any external shell command.
 3. As an example type   ls   following the ! and then hit <ENTER>.  This
    will show you a listing of your directory, just as if you were at the
    shell prompt.  Or use  :!dir  if ls doesn't work.

# Setting options

Typing ":set xxx" sets the option "xxx".  Some options are:

- 'ic' 'ignorecase'	ignore upper/lower case when searching
- 'is' 'incsearch'	show partial matches for a search phrase
- 'hls' 'hlsearch'	highlight all matching phrases

You can either use the long or the short option name.
Prepend "no" to switch an option off:   :set noic

# Getting help

Vim has a comprehensive on-line help system.  To get started, try one of
these three:

- press the <HELP> key (if you have one)
- press the <F1> key (if you have one)
- type   :help <ENTER>

Read the text in the help window to find out how the help works.
Type  CTRL-W CTRL-W   to jump from one window to another.
Type    :q <ENTER>    to close the help window.

You can find help on just about any subject, by giving an argument to the
":help" command.  Try these (don't forget pressing <ENTER>):

- :help w
- :help c_CTRL-D
- :help insert-index
- :help user-manual

## Links

- https://vim.fandom.com/wiki/Learn_to_use_help
