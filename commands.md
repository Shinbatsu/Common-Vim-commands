# List of Vim commands

## Note

> If command should be written in "EDIT" mode
> then he will has E! prefix otherwise ("COMMAND") C!)
> If before command written ":" so this is "Command Mode"(Esc to change)

## How to leave the Vim?! Esc+:q

## Commmand List

### Main commands

```tex
ESC                       Enable Command Mode(ECM)
hjkl                      Movement (h:left,j:down,k:up,l:right)
i                         Enable Edit Mode(EEM)
I                         EEM and go to start of line
a                         EEM and go to next char
A                         EEM and go to end of line
o                         EEM and go to next line
O                         EEM and go to previous line
R                         EEM and replace text over the current(key "Insert")
u, :u[ndo]                Undo(With Command Mode enanbled before)
CTR-R, :red[o]            Undo(With Command Mode enanbled before)
dd                        Cut line
cc                        Remove
yy                        Copy
p                         Paste
<n>d                      remove n+1 line
<n>y                      copy n+1 line
DEL                       remove next char
:<n>                      go to line number "n"
%                         goto to first pair of round brackets
:e **/filename.c          edit file with searching by name
:w [fname]                save changes 
:wa                       Save all
:q                        Leave(Exit)
:q!                       Leave without save(Exit)
:color <name>             Color schemes manager:/usr/local/share/vim/vim72/colors/*.vim
:pwd                      current directory
:cd [path]                change current edit directory
:!команда                 Run Command from Global(unix) environment - man, git, 
CTR+p или CTR+n           Autocomplete text(Edit Mode)
CTR+r,=,<expr>            Insert expression 5*2 - 3(Edit Mode)
CTR+u, CTR+d              
CTR+y, CTR+e              go up/down without changing cursor position          
```

### Highlits

```tex
:syntax on                enable highlit
:syntax off               diseable highlit (default)
```

### Wrap order

```tex
:set wrap                 Enable word wrap (default)
:set nowrap               Lock word wrap
```

### Printing

```tex
:ha[rdcopy]                   print doc
:set printoptions=duplex:off  disable two-side's print
```

### Expanding

```tex
== Expanding ==
zc                        Hide block
zo                        Show block
zM                        Hide all
zR                        Show all
za                        Inverse expanding
zf                        см :set foldmethod=manual
:set foldenable           enable expanding 
:set foldmethod=syntax    expanding by syntax
:set foldmethod=indent    expanding spaces
:set foldmethod=manual    select area by v and type zf for create your own block
:set foldmethod=marker    expanding by markers
:set foldmarker=bigin,end create start and end markers
```

### Markers

```tex
ma                        set local marker named "a"
mB                        set global marker named "B"
`c                        goto local marker "c"
`0                        return to position which was before current session
:marks                    marker list
```

### Sessions

```tex
mksession file.session    save current session
source file.session       recover prebious saved session
```

### Aliases

```tex
qa                        Create Aliases named a
q                         In Aliases Mode: exit
@a                        complete alias "a"
@@                        repeat last
```

### Selection

```tex
v + hjkl                  select all text
SHIFT + v                 select line
CTR + v                   select rectangle
p                         paste
y                         copy
d                         delete
gu                        change to upper case
gU                        change to upper case
```

### Local searching

```tex
/EXP                     searching an EXP in file
\cEXP                    searching an exprassion in file (register ignore)
n                        next match
N                        prev match
:%s/foo/bar/gi           regexp_replace,http://eax.me/regular-expr/
```

### Global searching

```tex
:vimgrep /RevExp/ **/*.c regular expression searching
:copen                   show all matched parts
:close                   hide all matched parts
:cn                      next match
:cp                      prev match
```

### Numeration

```tex
:set number              enable line numeration
:set nonumber            diseable line numeration
```

### Encoding

```tex
e ++enc=<utf-8>         Edit file in  <"utf-8"> encoding
w ++enc=<"utf-8">         Save file in<"utf-8"> encoding
set fileencodings=utf-8,koi8-r  Encoding listС
```

### More

```tex
:set [no]wildmenu          autocomplete word 
:set list                  Show tabs and spaces
q:                         Command history
.                          run last commnad
```
