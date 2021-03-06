#Bash Profile
This assumes you have brew installed and have set /etc/brashprof.conf

```shell
echo "source $PWD/.bash_profile" >> ~/.bash_profile
ln -s $PWD/.config $HOME/.config
ln -s $PWD/.gitconfig $HOME/.gitconfig
ln -s $PWD/.tmux.conf $HOME/.tmux.conf
mkdir -p ~/.vim/undodir
ln -s $PWD/.vimrc $HOME/.vimrc
ln -sf $PWD/sublime-text-3/Preferences.sublime-settings "$HOME/Library/Application Support/Sublime Text 3/Packages/User/Preferences.sublime-settings"
cat brew.txt | xargs brew install
```

Switch your default shell to the version of bash installed by brew (as pre-installed version on mac is out of date).
```shell
sudo sh -c 'echo /usr/local/bin/bash >> /etc/shells'
chsh -s /usr/local/bin/bash
```

Setup iTerm2
```shell
defaults write com.googlecode.iterm2.plist PrefsCustomFolder -string "$PWD/iterm2"
defaults write com.googlecode.iterm2.plist LoadPrefsFromCustomFolder -bool true
```

Install Source Code Pro font
```shell
brew tap caskroom/fonts
brew cask install font-source-code-pro
```
