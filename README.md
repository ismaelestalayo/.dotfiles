# Powershell

1- Install necessary modules:

```Powershell
Install-Module posh-git -Scope CurrentUser
Install-Module oh-my-posh -Scope CurrentUser
```

2- Then create a profile.ps1 with `notepad $PROFILE` and paste the following:

```Powershell
Set-PSReadLineOption -EditMode Emacs
Import-Module posh-git
Import-Module oh-my-posh
Set-Theme Paradox
```


3- (optional) If there's any problem with execution policies of the script at launch:

```Powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

# zsh

1- First install zsh with
```Bash
sudo apt install zsh
```

2- Then install oh-my-zsh

```Bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```


3- (optional) Install spaceship prompt:

```Bash
git clone https://github.com/denysdovhan/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt"
```

```Bash
ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"
```



4- (optional) install auto-suggestion plugin:

```Bash
git clone https://github.com/zsh-users/zsh-autosuggestions ~/.zsh/zsh-autosuggestions
```

## .zshrc file

```Bash
# Path to your oh-my-zsh installation.
export ZSH="/home/USERNAME/.oh-my-zsh"
 
# Set name of the theme to load
ZSH_THEME="spaceship"

# Uncomment the following line if pasting URLs and other text is messed up.
# DISABLE_MAGIC_FUNCTIONS=true

# Uncomment the following line to disable colors in ls.
# DISABLE_LS_COLORS="true"

# Uncomment the following line to enable command auto-correction.
# ENABLE_CORRECTION="true"

# Uncomment the following line to display red dots whilst waiting for completion.
COMPLETION_WAITING_DOTS="true"

# Which plugins would you like to load?
# Standard plugins can be found in ~/.oh-my-zsh/plugins/*
# Custom plugins may be added to ~/.oh-my-zsh/custom/plugins/
# Add wisely, as too many plugins slow down shell startup.
plugins=(git copyfile zsh-autosuggestions)

source $ZSH/oh-my-zsh.sh

# User configuration

# You may need to manually set your language environment
# export LANG=en_US.UTF-8

# Set personal aliases, overriding those provided by oh-my-zsh libs,
# plugins, and themes. Aliases can be placed here, though oh-my-zsh
# users are encouraged to define aliases within the ZSH_CUSTOM folder.
# For a full list of active aliases, run `alias`.

function lazygit() {
    if [ -z "$1" ]
        then
        echo "> must specify a commit message"
    else
        git add .
        git commit -a -m "$1"
        git push
    fi
}
```

# vim

## .vimrc file

```Bash
colorscheme slate
colorscheme koehler
set number 
syntax on 

set encoding=utf-8
set pastetoggle=<F2>

set scrolloff=3

set wrap
set textwidth=79

set tabstop=4
set shiftwidth=4
set softtabstop=4
set expandtab

set ttyfast
```

# tmux

## .tmux.conf

```Bash
# Enable mouse mode (tmux 2.1 and above) 
set -g mouse on

# Use Alt-arrow keys without prefix key to switch panes
bind -n M-Left select-pane -L
bind -n M-Right select-pane -R
bind -n M-Up select-pane -U
bind -n M-Down select-pane -D
```

