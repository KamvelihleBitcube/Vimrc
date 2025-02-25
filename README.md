# Vimrc
```
let mapleader=" "

"""Common Settings and Defaults
set scrolloff=5
set hlsearch
set incsearch
set relativenumber
set smartcase
map Q gq

""" Plugins

" Highlight copied text
Plug 'machakann/vim-highlightedyank'
Plug 'tpope/vim-commentary'
Plug 'tpope/vim-surround'
Plug 'easymotion/vim-easymotion'
Plug 'tommcdo/vim-exchange'
Plug 'vim-scripts/ReplaceWithRegister'
Plug 'mg979/vim-visual-multi', {'branch': 'master'}
Plug 'terryma/vim-multiple-cursors'
Plug 'justinmk/vim-sneak'
Plug "kshenoy/vim-signature"
Plug 'preservim/nerdtree'

" --- Set Plugins
set multiple-cursors
set vim-visual-multi
set commentary
set surround
set exchange
set signature
set ReplaceWithRegister
set NERDTree
set easymotion
"set sneak

" --- Plugin Settings
filetype plugin indent on
let g:exchange_no_mappings=1

" Exchange
nnoremap cx <Plug>(Exchange)

map X <Plug>(Exchange)
nmap cxc <Plug>(ExchangeClear)
nmap cxx <Plug>(ExchangeLine)

" JK motions: Line motions
nnoremap s{char}{char} <Plug>(easymotion-overwin-s2)
nmap <mapleader><mapleader>f <Plug>(easymotion-f)

nnoremap gt :NERDTree<CR>
"" -- Map IDE actions to IdeaVim
nmap [[ <Action>(MethodUp)
nmap ]] <Action>(MethodDown)

nnoremap gn :action GotoNextError<CR>
nnoremap gp :action GotoPreviousError<CR>
nnoremap ge :action ShowErrorDescription<CR>
nnoremap gh :action ShowHoverInfo<CR>


"" Map \r to the Reformat Code action
nnoremap \\r :action ReformatCode<CR>

"" Map <leader>d to start debug
map \d <Action>(Debug)

"" Map \b to toggle the breakpoint on the current line
map \b <Action>(ToggleLineBreakpoint)
```
