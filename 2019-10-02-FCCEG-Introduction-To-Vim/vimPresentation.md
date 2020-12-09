Vim: God's Editor
========================================================
author: Bryan Jenks
date: 20191004
autosize: true


History
========================================================

vi -> Vim -> NeoVim

28 Years Old (as of November 2nd) although vi is older

vi is on pretty much everything, servers, linux, mac OS

Vim is Written in C & VimScript so it is **FAST**

NeoVim is a fork (what im curently using)

Vim/NeoVim is FOSS

Bram Moolenaar (Creator of Vim) - Still maintaining it to date

Benefits
========================================================

- base competency is useful for server things
- When messing with CLI things, like git, or directory movement
- Using Vim can be much more ergonomic
- fingers never leave home row
- everything is on the keyboard
- no reaching for mouse
- **vim language**
- SYSTEM im using (Arch, LARBS, Terminal Apps)

Baby Steps
========================================================

**How to quit vim**  

`:q`   
`:q!`  
`:qw`  

Baby Steps
========================================================

**How to move**

`hjkl`

<s>arrow keys</s>  
<s>space to move forward</s>  
<s>bs to move backward</s>

Baby Steps
========================================================

**Modes**

- Normal <3
- Visual (Visual, Block, Line) <33
- Command
- Replace
- <s>Insert</s>

Baby Steps
========================================================

**Undo**

`u`

- Even macros can be undone
- Redo is done with \<CTRL\> + `r`

Baby Steps
========================================================

**Searching**

- `/` text to search for `enter`
- `n` to go to next find of that item
- `N` to go to previous find of that item

Baby Steps
========================================================

**Built In Spell Check**

- Yeah its in there, set your language dictionary first though
- `z=` in a selected word gives a list of suggestions
    + type a number
    + \<enter\> to replace
    
Text Objects
========================================================

- Word
    + Punctuation
- Sentence
- Paragraph

Text Objects + Numbered Motions
========================================================

- Delete numbers of characters
    + words
    + sentences
    + paragraphs
- Movement across a number of text objects

Line Folding
========================================================

- `:zf` Number of lines to fold followed by direction `jk`
- `:zo` open a line fold

Splits
========================================================

- `:sp` split horizontally
- `:vsp` split vertically
- _\<CTRL\>_ keys + motion keys `hjkl` to move between windows
- `:e` + Filename to open multiple files
    + \<tab\> completion will help you find your file

Macros
========================================================

- `q` + `a-z, A-Z, 0-9` to assin macro to register total of 62 spots
- To run macro `:@a`
- `@@` To run last macro ran
- To redo last action `.`

VIMRC
========================================================

- 'runtime configuration'
- put all settings and configurations here
- Custom mappings here
- Plugins Here

Custom Mappings
========================================================

- You can make custom key remaps
- \<leader\> commands for macros or snippets
- make snippets for same key combos based on file types

Plugins
========================================================

- Plugins for everything 
    + Nerd tree (File Tree)
    + goyo (Focus Mode)
    + vimwiki (WikiType Doc Management in Markdown)
    + airline (Status Bar)
    + **and more!**
- If desired, Vim can be an IDE (with lots of configuration)

Take Aways
========================================================

- Maybe not for everyone or for everything
- Lightweight/Fast/FOSS/Ubiquitos/Terminal/Chad
- Most IDE's have a _Vim Mode_
	+ EMACS (Evil mode)
	+ VS Code (Vim Extention)
	+ RStudio (built in Mode)
	+ Atom (plugin)
- The vim language and modal editing improves efficiency and your hands never leave the keyboard so even if not using vim, the language, modal editing, and efficiency gains over time are **monumental**.

Resources
========================================================

**Hyperlinks on Github!**

========================================================
**Thank You!**  
: )
