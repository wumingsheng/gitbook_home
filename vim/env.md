# vim环境配置



## 1. vimrc

```


" 这里先介绍一个插件镜像地址，官方的太卡https://vimawesome.com


" https://github.com/junegunn/fzf 
" https://github.com/junegunn/fzf.vim.git
" dependency out command fzf
" git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
" ~/.fzf/install


"  ctrl-t: tab split
"  ctrl-x: split
"  ctrl-v: vsplit

" command :FZF or :Files  


set rtp+=~/.fzf    " runtimepath

" sudo apt-get install silversearcher-ag
" 将:Ag命令可以在Vim内搜索项目内的文本了。
nmap <C-p> :Files<CR>

" $ cd ~/.vim/bundle
" $ git clone git://github.com/chase/vim-ansible-yaml.git






" -----------------------------------------------------------------------------
"  <　auto-pairs 插件配置:括号补全插件 >https://github.com/jiangmiao/auto-pairs
" -----------------------------------------------------------------------------


"--------------------------------------------------------
" https://vimawesome.com/plugin/vim-devicons
" 文件图标插件git clone https://github.com/ryanoasis/vim-devicons
"--------------------------------------------------------

" 系统默认的字体会出现乱码，需要安装nerd字体https://github.com/ryanoasis/nerd-fonts#patched-fonts

" 系统默认的字体会出现乱码，需要安装nerd字体
" 从这里选择中自己喜欢的字体下载https://github.com/ryanoasis/nerd-fonts#patched-fonts
" 例如我选择DroidSansMono字体 .ttf或者.otf文件
" linux安装字体
" cd /usr/share/fonts
" sudo mkdir DroidSansMono
" sudo mv /home/wms/Downloads/Droid\ Sans\ Mono\ Nerd\ Font\ Complete.otf DroidSansMono
" sudo mkfontscale
" sudo mkfontdir
" fc-cache
" fc-list|grep Droid
" ctrl + f11 调出gvim的菜单栏
" 设置字体为刚安装好的字体





















"------------------------------------------------
"goyo+limelight 
"----------------------------------------------







" -----------------------------------------------------------------------------
"  <　vim-auto-save 插件配置:自动保存插件 >https://github.com/907th/vim-auto-save
" -----------------------------------------------------------------------------

let g:auto_save = 1  " enable AutoSave on Vim startup
let g:auto_save_events = ["InsertLeave", "TextChanged"]
let g:auto_save_silent = 0  "  display the auto-save notification

"-----------------------
"https://github.com/plasticboy/vim-markdown
"-------------------------
let g:vim_markdown_folding_disabled = 1 " 禁用markdown折叠
let g:vim_markdown_toc_autofit = 1 " Enable TOC window auto-fit
let g:vim_markdown_folding_level = 6
let g:vim_markdown_conceal = 0


" -----------------------------------------------------------------------------
"  < indentLine 插件配置 >https://github.com/Yggdroot/indentLine
" 缩进线
" -----------------------------------------------------------------------------



"----------------------------------
" https://github.com/Shougo/deoplete.nvim
"-------------------------------
" Use deoplete.
set pyxversion=3
let g:deoplete#enable_at_startup = 1


"---------------------------------
"https://github.com/majutsushi/tagbar.git
"-----------------------------------------
" https://github.com/universal-ctags/ctags  这个是依赖，需要先安装 https://www.cnblogs.com/cascle/p/5133213.html
nmap <F8> :TagbarToggle<CR>
" 对markdown文件的支持
" let g:tagbar_ctags_bin = '/home/user/.vim/ctags/bin/'
let g:tagbar_type_markdown = {'ctagstype': 'markdown','ctagsbin' : '~/.vim/bundle/markdown2ctags/markdown2ctags.py','ctagsargs' : '-f - --sort=yes','kinds' : ['s:sections','i:images'],'sro' : '|','kind2scope' : {'s' : 'section',},'sort': 0,}





" -----------------------------------------------------------------------------
"  < vim-gitgutter 插件配置：git插件看状态 >git://github.com/airblade/vim-gitgutter.git
" -----------------------------------------------------------------------------


" -----------------------------------------------------------------------------
"  < vim-fugitive 插件配置：git插件　对比 >https://github.com/tpope/vim-fugitive.git
" -----------------------------------------------------------------------------
" 只用到一个命令：Gdiff其他的强大之处还没有发现





" -----------------------------------------------------------------------------
"  < vim-airline 插件配置：底栏美化插件 >https://github.com/vim-airline/vim-airline
" -----------------------------------------------------------------------------
let g:airline_powerline_fonts = 1

" -----------------------------------------------------------------------------
"  < supertab 插件配置：tab补全插件 >https://github.com/ervandew/supertab
" -----------------------------------------------------------------------------




" -----------------------------------------------------------------------------
"  < nerdcommenter 插件配置：注释插件 >https://github.com/scrooloose/nerdcommenter
" -----------------------------------------------------------------------------
" 我主要用于C/C++代码注释(其它的也行)
" 以下为插件默认快捷键，其中的说明是以C/C++为例的，其它语言类似
" <Leader>ci 以每行一个 /* */ 注释选中行(选中区域所在行)，再输入则取消注释
" <Leader>cm 以一个 /* */ 注释选中行(选中区域所在行)，再输入则称重复注释
" <Leader>cc 以每行一个 /* */ 注释选中行或区域，再输入则称重复注释
" <Leader>cu 取消选中区域(行)的注释，选中区域(行)内至少有一个 /* */
" <Leader>ca 在/*...*/与//这两种注释方式中切换（其它语言可能不一样了）
" <Leader>cA 行尾注释
let NERDSpaceDelims = 1                     "在左注释符之后，右注释符之前留有空格
" Add spaces after comment delimiters by default
" let g:NERDSpaceDelims = 1
" Use compact syntax for prettified multi-line comments
" let g:NERDCompactSexyComs = 1
" Align line-wise comment delimiters flush left instead of following code indentation
" let g:NERDDefaultAlign = 'left'
" Set a language to use its alternate delimiters by default
" let g:NERDAltDelims_java = 1
" Add your own custom formats or override the defaults
" let g:NERDCustomDelimiters = { 'c': { 'left': '/**','right': '*/' } }
" Allow commenting and inverting empty lines (useful when commenting a region)
" let g:NERDCommentEmptyLines = 1
" Enable trimming of trailing whitespace when uncommenting
" let g:NERDTrimTrailingWhitespace = 1
nmap <c-c> <Leader>ci<CR> " 定义ctrl+c作为注释快捷键









" -----------------------------------------------------------------------------
"  < vim-pathogen 插件配置：插件管理插件 >https://github.com/tpope/vim-pathogen
" -----------------------------------------------------------------------------
execute pathogen#infect()

filetype plugin indent on


" -----------------------------------------------------------------------------
"  < nerdtree 插件配置：文件目录结构插件 >https://github.com/scrooloose/nerdtree
" -----------------------------------------------------------------------------
" autocmd vimenter * NERDTree " 自动打开
 nmap <F2> :NERDTreeToggle<CR>
" 使用大写的Ｉ 可以显示隐藏的文件和文件夹
" 使用m操作节点/i.......使用一个水平分割窗口来打开选中的文件. /s.......使用一个垂直窗口来打开选中的文件 /r......刷新当前目录
" P.......跳到当前的根目录(什么是当前的根目录? 自己实际操作就明白了)/p.......跳到父目录
" x.......关闭当前节点的目录 /X.......关闭所选目录下的所有子目录
autocmd bufenter * if (winnr("$") == 1 && exists("b:NERDTree") && b:NERDTree.isTabTree()) | q | endif
" 显示行号
let NERDTreeShowLineNumbers=0
" 是否显示隐藏文件
let NERDTreeShowHidden=0
let NERDTreeIgnore=['\.pyc','\~$','\.swp']
let g:nerdtree_tabs_open_on_console_startup=1
autocmd vimenter * if !argc()|NERDTree|endif
" -----------------------------------------------------------------------------
"  < nerdtree-git-plugin 插件配置：文件目录结构插件 >https://github.com/xuyuanp/nerdtree-git-plugin
" -----------------------------------------------------------------------------
" gvim根目录必须是git仓库，nerdtree可以用CD切换目录

" o       在已有窗口中打开文件、目录或书签，并跳到该窗口
" go      在已有窗口 中打开文件、目录或书签，但不跳到该窗口
" t       在新 Tab 中打开选中文件/书签，并跳到新 Tab
" T       在新 Tab 中打开选中文件/书签，但不跳到新 Tab
" i       split 一个新窗口打开选中文件，并跳到该窗口
" gi      split 一个新窗口打开选中文件，但不跳到该窗口
" s       vsplit 一个新窗口打开选中文件，并跳到该窗口
" gs      vsplit 一个新 窗口打开选中文件，但不跳到该窗口
" !       执行当前文件
" O       递归打开选中 结点下的所有目录
" x       合拢选中结点的父目录
" X       递归 合拢选中结点下的所有目录
" e       Edit the current dif
" D       删除当前书签
" P       跳到根结点
" p       跳到父结点
" K       跳到当前目录下同级的第一个结点
" J       跳到当前目录下同级的最后一个结点
" k       跳到当前目录下同级的前一个结点
" j       跳到当前目录下同级的后一个结点
" C       将选中目录或选中文件的父目录设为根结点
" u       将当前根结点的父目录设为根目录，并变成合拢原根结点
" U       将当前根结点的父目录设为根目录，但保持展开原根结点
" r       递归刷新选中目录
" R       递归刷新根结点
" m       显示文件系统菜单
" cd      将 CWD 设为选中目录
" I       切换是否显示隐藏文件
" f       切换是否使用文件过滤器
" F       切换是否显示文件
" B       切换是否显示书签




"-------------------------------------
"语法检查https://github.com/vim-syntastic/syntastic
"----------------------------------
set statusline+=%#warningmsg#
set statusline+=%{SyntasticStatuslineFlag()}
set statusline+=%*

let g:syntastic_always_populate_loc_list = 1
let g:syntastic_auto_loc_list = 1
let g:syntastic_check_on_open = 1
let g:syntastic_check_on_wq = 0





" -----------------------------------------------------------------------------
"  < solarized 插件配置：主题插件 >https://github.com/altercation/vim-colors-solarized
" -----------------------------------------------------------------------------

" set background=dark
" colorscheme solarized

" -----------------------------------------------------------------------------
"  < gruvbox 插件配置：主题插件 >https://github.com/morhetz/gruvbox
" -----------------------------------------------------------------------------
colorscheme gruvbox
set background=dark
let g:gruvbox_contrast_dark='soft'


" https://vimawesome.com/plugin/vim-nerdtree-tabs




set fileencodings=utf-8,ucs-bom,gb18030,gbk,gb2312,cp936    "  打开文件中文乱码
set termencoding=utf-8
set encoding=utf-8
set autoindent
set nu
set number
set textwidth=100
set matchtime=2 "短暂跳转到匹配括号的时间
syntax on
filetype on
filetype plugin on                                    "针对不同的文件类型加载对应的插件
set smartindent                                      "开启新行时使用智能自动缩进 
set expandtab                                         "将Tab键转换为空格

set smarttab                                          "指定按一次backspace就删除shiftwidth宽度的空格
set cursorline                                        " 突出显示当前行
set autoread                                          " 当文件在外部被修改，自动更新该文件
set hlsearch                                          "高亮搜索
set incsearch                                         "搜索实时匹配
set ignorecase                                        "搜索模式里忽略大小写
set smartcase                                         "如果搜索模式包含大写字符，不使用 'ignorecase' 选项，只有在输入搜索模式并且打开 'ignorecase' 选项时才会使用
set laststatus=2                                   "启用状态栏信息
set cmdheight=1                                      "设置命令行的高度为2，默认为1
" set nowrap                                            "设置不自动换行
set wrap                                            "设置自动换行
set shortmess=atI                                     "去掉欢迎界面
" 文件格式，默认 ffs=dos,unix
set fileformat=unix                                   "设置新文件的<EOL>格式
set fileformats=unix,dos,mac                          "给出文件的<EOL>格式类型
set guifont=Monospace\ 12                 "设置字体:字号（字体名称空格用下划线代替）
set mouse=a                    " 在任何模式下启用鼠标
set foldenable                                        "启用折叠
" set foldmethod=indent                                 "indent 折叠方式
nnoremap <space> @=((foldclosed(line('.')) < 0) ? 'zc' : 'zo')<CR> " 用空格键来开关折叠
set breakindent
set linebreak
set mousemodel=popup                                   "开启右键快捷方式
" set guioptions+=b                                    "添加水平滚动条
set selection=inclusive                          "选择文本时光标所在的位置也被选中
set selectmode=    "不适用selectmode
set keymodel=   
set wildmenu    
set wildmode=full
set whichwrap=b,s,<,>,[,]
"set spell                                      "拼写检查
set ru
set sm
set backspace=indent,eol,start whichwrap+=<,>,[,]
set ai " 自动缩进，新行与前面的行保持—致的自动空格
set aw  " 自动写，转入shell或使用：n编辑其他文件时，当前的缓冲区被写入
set flash                     " 在出错处闪烁但不呜叫(缺省)
set ic                          " 在查询及模式匹配时忽赂大小写
set cin
set lbr
set fo+=mB
set ambiwidth=double
set nocp
set nocompatible " 防止进入vi兼容模式
set nobackup
set noswapfile
set history=1024
set autochdir
set clipboard+=unnamed          " Vim 的默认寄存器和系统剪贴板共享
set winaltkeys=no         " 设置 alt 键不映射到菜单栏

set showmatch          " 显示括号配对，当键入“]”“)”时，高亮度显示匹配的括号
set showmode           " 处于文本输入方式时加亮按钮条中的模式指示器
set showcmd             " 在状态栏显示目前所执行的指令，未完成的指令片段亦会显示出来
set warn       " 对文本进行了新的修改后，离开shell时系统给出显示(缺省) /nowarn 
set ws            " 在搜索时如到达文件尾则绕回文件头继续搜索 /nows   
set cindent                 " 以C/C++的模式缩进
" set noignorecase       " 默认区分大小写
set ruler                     " 打开状态栏标尺
set scrolloff=5            " 设定光标离窗口上下边界 5 行时窗口自动滚动


syntax on
syntax enable
" set lines=1000 
" set columns=1000 
set helplang=cn
" set nohlsearch "取消高亮显示 （查找字符串是，找到后高亮显示）
set incsearch "在输入搜索的字符串同时就开始搜索已经输入的部分

" 启用每行超过80列的字符提示（字体变蓝并加下划线），不启用就注释掉
" au BufWinEnter * let w:m2=matchadd('Underlined', '\%>' . 80 . 'v.\+', -1)

set writebackup                             "保存文件前建立备份，保存成功后删除该备份
set nobackup                                "设置无备份文件
" set noswapfile                              "设置无临时文件
set vb t_vb=                                "关闭提示音



set softtabstop=2      " 使得按退格键时可以一次删掉 4 个空格,不足 4 个时删掉所有剩下的空格）
set tabstop=2                                        "设置Tab键的宽度
set shiftwidth=2        " 设定 << 和 >> 命令移动时的宽度为 4


set nrformats=





" -----------------------------------------------------------------------------
"  < 判断是终端还是 Gvim >
" -----------------------------------------------------------------------------
if has("gui_running")
    let g:isGUI = 1
else
    let g:isGUI = 0
endif

" 显示/隐藏菜单栏、工具栏、滚动条，可用 Ctrl + F11 切换
if g:isGUI
    set guioptions-=m
    set guioptions-=T
    set guioptions-=r
    set guioptions-=L
    map <silent> <c-F11> :if &guioptions =~# 'm' <Bar>
        \set guioptions-=m <Bar>
        \set guioptions-=T <Bar>
        \set guioptions-=r <Bar>
        \set guioptions-=L <Bar>
    \else <Bar>
        \set guioptions+=m <Bar>
        \set guioptions+=T <Bar>
        \set guioptions+=r <Bar>
        \set guioptions+=L <Bar>
    \endif<CR>
endif

" 设置 gVim 窗口初始位置及大小
"if g:isGUI
"   " au GUIEnter * simalt ~x                           "窗口启动时自动最大化
"   winpos 100 10                                     "指定窗口出现的位置，坐标原点在屏幕左上角
"   set lines=38 columns=120                          "指定窗口大小，lines为高度，columns为宽度
"ndif





" 屏幕行和实际行移动键统一
nnoremap k gk
nnoremap gk k
nnoremap j gj
nnoremap gj j


" :tabnew 创建新的tab
" :tabc 关闭当前的tab
" :tabo 关闭其他的tabs
" :tabn 切换tab
" :bn 下一个文件
" :bp 上一个文件



" normal模式下,同一个文件中,回到上次修改的地方,再回来 ctrl + o  ctrl + i














```


## 2. 插件列表




- ansible-snippets
- ansible-vim
- auto-pairs
- fcitx.vim
- fzf
- fzf.vim
- goyo.vim
- gruvbox
- indentLine
- limelight.vim
- markdown2ctags
- neoterm
- nerdcommenter
- nerdtree
- nerdtree-git-plugin
- nvim-yarp
- powerline
- supertab
- syntastic
- tagbar
- vim-airline
- vim-auto-save
- vim-colors-solarized
- vim-fugitive
- vim-gitgutter
- vim-go
- vim-hug-neovim-rpc
- Vim-Jinja2-Syntax
- vim-markdown
- vim-nerdtree-tabs
- vim-nginx
- vim-surround
- vim-textobj-entire
- vim-textobj-user
- ZoomWin








