# Powershell

Currently using the PowerShell 7.1 preview (from store for auto updates) which I've also customized to be inline with my
zsh prompt.

1- Install necessary modules:

```Powershell
Install-Module posh-git -Scope CurrentUser
```

2- Then create/edit a profile.ps1 with `vim $PROFILE` (you can use notepad as well) and paste the following:

```Powershell
Set-PSReadLineOption -EditMode Emacs
Import-Module posh-git
```

3- Modify your prompt

```Powersshell
# Add a new line before and after your prompt
$GitPromptSettings.DefaultPromptSuffix = '`n▶ '
$GitPromptSettings.DefaultPromptPrefix = '`n'
```


*(optional)* If there's any problem with execution policies of the script at launch:

```Powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```


4- Personalize the Windows Terminal

Use [settings.json](settings.json)




<br></br>
# bash

Enable case-insensitive auto-completion
```bash
echo 'set completion-ignore-case On' | sudo tee -a /etc/inputrc
```

Lightweight personalized prompt:

```bash
export PS1='\[\e[38;5;12m\] \n$PWD \[\e[38;5;28m\] \n\\$\[$(tput sgr0)\] '
```

It's always handy to make a few symbolic links to the Windows files you wanna access:
```bash
ln -s /mnt/c/Users/<username> .
```




<br></br>
# zsh

1- First install zsh with
```Bash
sudo apt install zsh
```

2- Then install oh-my-zsh

```Bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```


3- (optional) install auto-suggestion plugin:

```Bash
git clone https://github.com/zsh-users/zsh-autosuggestions ~/.zsh/zsh-autosuggestions
```

## .zshrc file

```Bash
# Path to your oh-my-zsh installation.
export ZSH="/home/USERNAME/.oh-my-zsh"

ZSH_THEME="avit"

COMPLETION_WAITING_DOTS="true"

# Which plugins would you like to load?
# Standard plugins can be found in ~/.oh-my-zsh/plugins/*
# Custom plugins may be added to ~/.oh-my-zsh/custom/plugins/
# Add wisely, as too many plugins slow down shell startup.
plugins=(git zsh-autosuggestions)

source $ZSH/oh-my-zsh.sh

cd
```
