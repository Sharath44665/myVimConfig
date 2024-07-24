# myVimConfig
simple vim configuration

- create file `.vimrc` in home directory

inside `.vimrc`

``` vi
set number
set mouse=a

inoremap { {}<Esc>ha
inoremap ( ()<Esc>ha
inoremap [ []<Esc>ha
inoremap " ""<Esc>ha
inoremap ' ''<Esc>ha
inoremap ` ``<Esc>ha


call plug#begin()

" List your plugins here
Plug 'tpope/vim-sensible'

call plug#end()
```


