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

if has("autocmd")
  au VimEnter,InsertLeave * silent execute '!echo -ne "\e[2 q"' | redraw!
  au InsertEnter,InsertChange *
\ if v:insertmode == 'i' | 
\   silent execute '!echo -ne "\e[6 q"' | redraw! |
\ elseif v:insertmode == 'r' |
\   silent execute '!echo -ne "\e[4 q"' | redraw! |
\ endif
au VimLeave * silent execute '!echo -ne "\e[ q"' | redraw!
endif
```
continue the following inside `.vimrc`
refer to this 👉 [link](https://github.com/junegunn/vim-plug) 👈

```
call plug#begin()

" List your plugins here
Plug 'tpope/vim-sensible'

call plug#end()
```

## Tip: how to reload file in console

```
source file_name
```

