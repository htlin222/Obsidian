# Shell Command for Init

先裝完後再裝python不然會把zshrc重置

```bash=
# download zsh
brew install zsh
brew install tmux

# download onhmyzsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
# change shell to zsh
sudo sh -c "echo $(which zsh) >> /etc/shells"
chsh -s $(which zsh)
git clone https://github.com/bhilburn/powerlevel9k.git ~/.oh-my-zsh/custom/themes/powerlevel9k
brew tap homebrew/cask-fonts
brew install --cask font-meslo-for-powerline

git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting


```

```shell=
vim ~/.zshrc
```
### .zshrc setting

```txt=
# aliasis...

ZSH_THEME="powerlevel9k/powerlevel9k"
POWERLEVEL9K_RIGHT_PROMPT_ELEMENTS=(status root_indicator background_jobs history time)
POWERLEVEL9K_LEFT_PROMPT_ELEMENTS=(context dir vcs)

ZSH_AUTOSUGGEST_HIGHLIGHT_STYLE='fg=30'

plugins=( 
    # other plugins...
    zsh-autosuggestions
	zsh-syntax-highlighting
)

```

```shell=
exec $SHELL
```


> Preferences -> Profiles -> Text -> Font -> Meslo Dotted for Powerline

