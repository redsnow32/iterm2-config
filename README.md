# iterm2-config

## Terminal setup utilizing iTerm2, tmux, tmuxinator and Oh-My-ZSH

The goal of this document is to show my current terminal setup utilizing iTerm2, tmux, turminator, zsh, and Oh-my-ZSH. I installed all dependents utilizing [Homebrew](https://brew.sh/).

##**Setup**

Install [Homebrew](https://brew.sh/)

    /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

Install [iTerm2](https://www.iterm2.com)

- Homebrew:

      brew cask install iterm2

- Manually:

  1. Click the download link included on the page provided above.

  2. Click and drag the iterm icon from your Downloads folder to the Applications folder.

  ![iTerm-Application](https://gist.githubusercontent.com/redsnow32/2b96d17fada6e0832888497d7c773c5a/raw/f43adcdfd231c06e0b2a42e7b55db5121be7790e/iterm-download.png)

iTerm2 allows you to customize your terminal colors and font settings. You can read more about customizations [here](https://sourabhbajaj.com/mac-setup/iTerm/)

Install tmux

    brew install tmux

Install tmuxinator

    gem install tmuxinator
