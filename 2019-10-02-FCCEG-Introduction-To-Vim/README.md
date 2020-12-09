![](images/vimlogo.png)

# Vim: God's Editor

## Outline:

## History

vi :arrow_right: [Vim](https://github.com/vim/vim) :arrow_right: NeoVim :heart:

[28 years old](https://bit.ly/1eoGZzD) (as of November 2nd) although vi is older

vi is on pretty much everything, servers, linux, mac OS

Vim is Written in C & VimScript so it is **FAST**

NeoVim is a fork (what im curently using)

Vim/NeoVim is FOSS

Bram Moolenaar (Creator of Vim) - Still maintaining it to date

### Benefits

- base competency is useful for server things
- When messing with CLI things, like git, or directory movement
- Using Vim can be much more ergonomic
- fingers never leave home row
- everything is on the keyboard
- no reaching for mouse
- **vim language**
- SYSTEM im using ([Arch](https://www.archlinux.org/), [LARBS](https://larbs.xyz/), Terminal Apps)

### Baby steps

#### How to quit vim

`:q`
`:q!`
`:qw`

#### How to move

`hjkl`

~~arrow keys~~

~~space to move forward~~

~~bs to move backward~~

#### Modes

- Normal (:heart:)
- Visual (Visual, Block, Line) (:sparkling_heart:)
- Command
- Replace
- Insert (:x:)

#### Undo

- `u`
- Even macros can be undone
- Redo is done with \<CTRL\> + `r`

#### Searching

- `/` text to search for `enter`
- `n` to go to next find of that item
- `N` to go to previous find of that item

#### Built In Spell Check

- Yeah its in there, set your language dictionary first though
- `z=` in a selected word gives a list of suggestions
    + type a number
    + \<enter\> to replace

### Text Objects

- Word
	+ Punctuation
- Sentence
- Paragraph

### Combining Text Objects With Numbers Actions/Motions

- Delete numbers of characters
    + words
    + sentences
    + paragraphs
- Movement across a number of text objects

### Line Folding

- `:zf`Number of lines to fold followed by direction`jk`
- `:zo` open a line fold

### Splits

- `:sp` split horizontally
- `:vsp` split vertically
- _\<CTRL\>_ keys + motion keys `hjkl` to move between windows
- `:e` + Filename to open multiple files
    + \<tab\> completion will help you find your file

### Macros

- `q` + `a-z, A-Z, 0-9` to assin macro to register total of 62 spots
- To run macro `:@a`
- `@@` To run last macro ran
- To redo last action `.`

### VIMRC's

- 'runtime configuration'
- put all settings and configurations here
- Custom mappings here
- Plugins Here

### Custom Mappings

- You can make custom key remaps
- \<leader\> commands for macros or snippets
- make snippets for same key combos based on file types

### Plugins

- Plugins for everything
    + Nerd tree (File Tree)
    + goyo (Focus Mode)
    + vimwiki (WikiType Doc Management in Markdown)
    + airline (Status Bar)
    + **and more!**
- If desired, Vim can be an IDE (with lots of configuration)

## Take Aways

- Maybe not for everyone or for everything
- Lightweight/Fast/FOSS/Ubiquitos/Terminal/Chad
- Most IDE's have a _Vim Mode_
	+ EMACS (Evil mode)
	+ VS Code (Vim Extention)
	+ RStudio (built in Mode)
	+ Atom (plugin)
- The vim language and modal editing improves efficiency and your hands never leave the keyboard so even if not using vim, the language, modal editing, and efficiency gains over time are **monumental**.

## resources:

### Youtube:

- [Your First Vim Plugin](https://www.youtube.com/watch?v=lwD8G1P52Sk)
- [Vim Playlist by Luke Smith](https://www.youtube.com/watch?v=ez1XBUqbS68&list=PL-p5XmQHB_JSTaEPygu1DZjuFfb704Uv7) :star: :star: :star: :star: :star:
- [Vim Line Folding screen cast](https://www.youtube.com/watch?v=oqYQ7IeDs0E)
- [Some Cool Vim Stuff](https://www.youtube.com/watch?v=aHm36-na4-4)
- [Thoughtbot Vim Talk are rad](https://www.youtube.com/results?search_query=thoughtbot+vim)

### Websites:

- [Vim - Github](https://github.com/vim/vim)
- [NeoVim](https://github.com/neovim/neovim)
- [VimAwesome Plugins](https://vimawesome.com/)

### Articles:

- [Wikipedia](https://bit.ly/1eoGZzD)

### Etc

- vimtutor in your terminal
- [Vim.org](https://www.vim.org/)
