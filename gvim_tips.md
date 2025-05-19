How to sort in gvim:

`:sort`

How to sort and keep only the unique lines in gvim:

`:sort u`

How to print only the word that matches a regular expression using grep
`grep -o "\w*<pattern>\w*" <filename>`

How to add mapping

`:map <space> viw`

Add the following to your ~/.vimrc file:

```
augroup filetype_html
    autocmd!
    autocmd FileType html nnoremap <buffer> <localleader>f Vatzf
augroup END
```
We enter the filetype_html group, immediately clear it, define an autocommand, and leave the group. If we source ~/.vimrc again the clearing will prevent Vim from adding duplicate autocommands.

Create a mapping for quickly source your vimrc

How to search for multiple patterns in gvim at the same time?

`/\(pattern1\|pattern2\)`

Below are some lines from my vimrc

" Use jk to go to escape mode and save file 
inoremap jk <Esc>:w!<CR>
" Use F7 for commenting out a link in verilog style
noremap <F7> 0i//
" Use F9 to surround the word under cursor with curly braces
noremap <F9> bi{ea}
" Use space to enter visual mode and select the word under the cursor
noremap <space> viw

References
```
https://learnvimscriptthehardway.stevelosh.com/
```
