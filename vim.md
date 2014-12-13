Vim workflow
------------

### NERDTree

**Show menu**

Type `m` while in NERDTree

**Open in tab**

Type `t` while in NERDTree

**Switch tabs**

`gt` next tab

`gT` previous tab

**Navigate by directory**

`command + t` open
`ctrl + t` open in tab

**Switch window**

`ctrl + w/W`

**Split window**

`:Vex/:Sex`

### Buffer

**List buffer**

`ls`

**Add a file to the buffer without opening**

`:badd foo.txt`

**Jump to a buffer**

`:buffer <num/path>`

**Delete a buffer**

`:bdelete <num/path>`

### Text Navigation

**Move the cursor**
`k` up
`j` down
`h` left
`l` right

**Move cursor to the beginning or end of a word**

`b` begin
`e` end

**Move the cursor word by word with whitespace as delimiter**

`B/E`

### Text Manipulation

**Paste**

`p`

**Insert a new line below**

`o`

**Cut the text in current quotes**

`:ci"`

**Remove line**

`dd`

**Delete from cursor to the end of the word**

`de`

**Delete until the next space**

`dE`

**Delete current word**

`diw`

**Delete within the current parentheses**
`di(`

**Delete text between quotes**

`di"`

**Yank text from here to the end of the word**

`ye` / `yE`

**Copy current word**

`bye`

**Copy current line**

`yy`

**Cut current line**

`cc`

**Move current line one row down**

`ddp`

### Tricks

**Output command into window**

`:.!` [command]
`:.! date` => outputs current date
