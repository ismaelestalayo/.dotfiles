# zsh (1)

install zsh:

`sudo apt install zsh`

install oh-my-zsh:

`sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"`

install spaceship prompt:

`git clone https://github.com/denysdovhan/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt"`

`ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme" `

# .zshrc (2)

``` 
ZSH_THEME="spaceship"
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
