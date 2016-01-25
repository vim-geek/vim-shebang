# vim-shebang

A simple plugin to insert the correct shebang of the file.

## Install

[vim-plug](https://github.com/junegunn/vim-plug)

```vimscript
Plug 'sbdchd/vim-shebang'
```

## Usage

Run the command `:ShebangInsert` or use an autocmd e.g., `au! BufNewFile * ShebangInsert`.

Normally, `:ShebangInsert` will not overwrite an existing shebang.
By calling the command with a bang, `:ShebangInsert!`, any existing shebang
will be overwritten.

Additionally, a shebang can be specified by passing a name/filetype to `:ShebangInsert`.

`:ShebangInsert python` or `:ShebangInsert node`

You can also directly pass your desired shebang to the function.

`:ShebangInsert #!/bin/sh`

## Config

To add/change/remove a shebang and filetype, simple create the dictionary `g:shebang#shebangs`
in your `.vimrc`.

```vimscript
let g:shebang#shebangs = {
            \ 'python': '#!/bin/python',
            \ 'sh': '',
            \ 'newfiletype': '#!/bin/newshebang'
            \ }
```
