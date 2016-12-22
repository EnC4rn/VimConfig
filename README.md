# Cerni's VimConfig
##  A vim configuration as learning material for dummy and beginner.
This Vim Configuration created to utilise mainly for lite coding and writing. It is optimised to work on Markdown, JS, C#, XML, HTML and CSS. I make this as clean as possible and you definitely need to access the specific files to do specific things. I do give comment to almost all configuration listed here, so you can see them as 'cheat sheet', especially for people who are new to vim and want to make configuration.

I divide this VimConfig into several files:

| File | Contents |
| --- | --- |
| .vimrc | Main configuration which shown at ~/ |
| .vimrc.plugins | all plugin used in this configuration |
| .vimrc.config | main configuration, you usually see this within main .vimrc |
| .vimrc.keymaps | all keymaps to native vim command. Plugin's specific keymap not included here |
| .vimrc.plugin.config | configuration for plugins used in this vim configuration. Including keymaps |

Again, you **definitely** need to add your custom configuration in those specific file, especially the plugins since plugin and plugin configuration will not work if the order is upside down.

![](VimConfig/myvim.PNG)

## Requirements
You need these dependency before you can use this config:
- Vim built with python, you can use the installer [here](https://github.com/vim/vim-win32-installer/releases/tag/v8.0.0003)
- [Git for Windows](https://git-for-windows.github.io/)
- [Python](https://www.python.org/downloads/)

## Folder structure
The folder structure of this vim configuration is here:

```sh
    ~\
    +---.vimrc
    |
    +---\VimConfig
    |   +---.vimrc.plugins
    |   +---.vimrc.config
    |   +---.vimrc.keymaps
    |   +---.vimrc.plugin.config
    |
    +---\.vim
    |   \---\bundles
    |
    +---\.vimview
    +---\.vimswap
    +---\.vimbackup
    +---\.vimundo
```

Please note that the `~\` means `%USERPROFILE%` or `C:\Users\[Your User]`

## GUI configuration
### Tab & Space
I use space instead of tab, so I map tab button to add 4 spaces. You can comment this if you are a tab user.

### Folding
I use syntax folding, if you want to use other folding style globally, please refer to `:h fold`. You can change using your preferred folding methods.

### Theme
I use the [gruvbox](https://github.com/morhetz/gruvbox) colorscheme in this configuration. You can use your own preferred colorscheme. Just put it at .vimrc.plugins and install it. This configuration use dark background as default.

### Font
The font used here is [FuraMonoPowerline_NF](https://github.com/ryanoasis/nerd-fonts/blob/master/patched-fonts/FiraMono), you can browse ryanoasis' repo [Nerd Fonts](https://github.com/ryanoasis/nerd-fonts) to find the font that suit you. Please use the font that support powerline in order for the vim airline powerline symbol to works correctly.

## Keymaps
### leader key
The default leader key used at vim is `\`, which is hard to reach, so I map the key into `,`. Feel free to map or comment out the mapleader as you see fit.

### $ key
$ key used to go to the end of line, since I'm using my own custom keyboard (VBLX-dvorak) derived from Programmer-Dvorak, the $ located at tilde (~) key, which is very far, therefore I swap the key with `q`. This may not make sense for QWERTY user, so feel free to comment it out.

### Navigation between split
I have eliminate the need to press `<C-W>` before `<C-[navigation key]>` to navigate between split. So when you need to jump to other split, just press `<C-[direction]>`. Ex: `<C-H>` will jump you to left split, while `<C-K>` will jump you to top split.

### Some shortcut
Here are some shortcut you might find interesting.

| shortcut | functions |
| --- | --- |
| `,bg` | switch background between dark and light |
| `,ns` | set nospell, useful when you hate those error mark at writing markdown |
| `F5` | Insert current timestamp |
| `,{1..x}` | open the buffer at number x |
| `F7` | Invoke TagbarToggle |
| `F8` | Invoke GundoToggle |
| `<C-E>` | Toggle NERDTree |
| `,sp` | implement :SoftPencil |

## Plugins
I use [Vundle](https://github.com/VundleVim/Vundle.vim) for plugin manager.

These are the plugins I put in this configuration:

| Plugin | Function | Link |
| --- | --- | --- |
| YouCompleteMe | Code Completion, you need to build it before it works | [Link](https://github.com/Valloric/YouCompleteMe) |
| UltiSnips | Syntax snippet | [Link](https://github.com/sirver/ultisnips) |
| Gundo | Undo history | [Link](https://github.com/sjl/Gundo.vim) |
| vimproc | run command and got result from within vim | [Link](https://github.com/shougo/vimproc.vim) |
| vimshell | a shell, within vim, nuff said | [Link](https://github.com/shougo/vimshell.vim) |
| tagbar | code tags | [Link](https://github.com/majutsushi/tagbar) |
| vim-airline | status bar for vim | [Link](https://github.com/bling/vim-airline) |
| numbers | better line number | [Link](https://github.com/myusuf3/numbers.vim) |
| syntastic | showing your code is wrong | [Link](https://github.com/scrooloose/syntastic) |
| vim-snippets | snippets for UltiSnips | [Link](https://github.com/honza/vim-snippets) |
| vim-surround | Working with surrounding symbol | [Link](https://github.com/tpope/vim-surround) |
| colorizer | view color of your hex within text | [Link](https://github.com/lilydjwg/colorizer) |
| nerd-commenter | commenting at vim made easy | [Link](https://github.com/scrooloose/nerdcommenter) |
| autoclose | autoclose surrounding symbol | [Link](https://github.com/Townk/vim-autoclose) |
| closetag | autoclose for HTML tag | [Link](https://github.com/vim-scripts/closetag.vim) |
| wakatime | track your active time, you need to register to [wakatime.com](https://wakatime.com/) first | [Link](https://github.com/wakatime/vim-wakatime) |
| fugitive | all about git utility | [Link](https://github.com/tpope/vim-fugitive) |
| NERDTree | file exlporer within vim | [Link](https://github.com/scrooloose/nerdtree) |
| ctrlpvim | mru, file and buffer explorer | [Link](https://github.com/ctrlpvim/ctrlp.vim) |
| gitgutter | git edit indicator at editor | [Link](https://github.com/airblade/vim-gitgutter) |
| NERDTree git plugin | git indicator at NERDTree | [Link](https://github.com/Xuyuanp/nerdtree-git-plugin) |
| vim pencil | Writer tools, especially wrapping | [Link](https://github.com/reedes/vim-pencil) |
| startify | a start page for vim | [Link](https://github.com/mhinz/vim-startify) |
| devicons | icons...for vim | [Link](https://github.com/ryanoasis/vim-devicons) |

## Language pack
I have these language pack plugin installed:

- [Mustache](https://github.com/mustache/vim-mustache-handlebars) by mustache
- [vim-javascript](https://github.com/pangloss/vim-javascript) by Pangloss
- [html5](https://github.com/othree/html5.vim) by Othree
- [css](https://github.com/JulesWang/css.vim) by JulesWang
- [markdown](https://github.com/gabrielelana/vim-markdown) by Gabrielelana
- [C#](https://github.com/OmniSharp/omnisharp-vim) by Omnisharp. You need to build this one.

## Last word
Personally, I don't really encourage to depend on anyone's configuration, but indeed, they are a good start for a new user of vim. You can understand how .vimrc actually works. I don't do many keymap because I don't needed them yet. I will add more if I find something I need. You can contact me if you having difficulty setting up your Vim. I will help as I can.
