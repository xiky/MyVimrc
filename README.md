# MyVimrc

" Configuration file for vim
set modelines=0		" CVE-2007-2438

" Normally we use vim-extensions. If you want true vi-compatibility
" remove change the following statements
set nocompatible	" Use Vim defaults instead of 100% vi compatibility
set backspace=2		" more powerful backspacing

" Don't write backup file if vim is being called by "crontab -e"
au BufWrite /private/tmp/crontab.* set nowritebackup nobackup
" Don't write backup file if vim is being called by "chpass"
au BufWrite /private/etc/pw.* set nowritebackup nobackup
syntax on
" 语法高亮

autocmd InsertLeave * se nocul
" autocmd InsertEnter * se cul
" 用浅色高亮当前行

set tabstop=4
" Tab键的宽度

set softtabstop=4
set shiftwidth=4
"  统一缩进为4

set number
" 显示行号

colorscheme pablo
" 设置颜色主题

set ruler
" 在编辑过程中，在右下角显示光标位置的状态行

set mouse=i
" 设置鼠标可用
" The mouse can be enabled for different modes:
"               n      Normal mode
"               v      Visual mode
"               i       Insert mode
"               c      Command-line mode
"               h      all previous modes when editing a help file
"               a      all previous modes
"               r      for |hit-enter| and |more-prompt| prompt
" Normally you would enable the mouse in all four modes with:
"              :set mouse=a
" When the mouse is not enabled, the GUI will still use the mousefor
" modeless selection.  This doesn't move the textcursor.


set scrolloff=3
" 光标移动到buffer的顶部和底部时保持3行距离
