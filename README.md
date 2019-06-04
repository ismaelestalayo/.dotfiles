# zsh (1)

install zsh:

`sudo apt install zsh`



install oh-my-zsh:

`sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"`



install spaceship prompt:

`git clone https://github.com/denysdovhan/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt"`

`ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme" `



install auto-suggestion plugin:

`git clone https://github.com/zsh-users/zsh-autosuggestions ~/.zsh/zsh-autosuggestions`

# .zshrc (2)

``` 
# Path to your oh-my-zsh installation.
export ZSH="/home/ismael/.oh-my-zsh"
 
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

# .vimrc

```
colorscheme slate       # or koehler
set number 
:syntax on 

set tabstop=4
set scrolloff=3
set pastetoggle=<F2>
```

# .tmux.conf

```
# Enable mouse mode (tmux 2.1 and above) 
set -g mouse on
```
