# iTerm2-tmux Setup

## Terminal setup utilizing iTerm2, zsh, and tmux

The goal of this document is to show my current terminal setup utilizing iTerm2, zsh, Oh-my-ZSH, tmux and turminator. All dependents were installed utilizing [Homebrew](https://brew.sh/). This setup is especially helpful as a full stack engineer; It allows me to run all of my apps/services in one terminal session.

##Setup

Install [Homebrew](https://brew.sh/)

    /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

---

Install [iTerm2](https://www.iterm2.com)

- Homebrew:

      brew cask install iterm2

- Manually:

  - Click the download link included on the page provided above

  - Click and drag the iterm icon from your Downloads folder to the Applications folder

  ![iTerm-Application](https://gist.githubusercontent.com/redsnow32/2b96d17fada6e0832888497d7c773c5a/raw/f43adcdfd231c06e0b2a42e7b55db5121be7790e/iterm-download.png)

Restart terminal

- iTerm2 allows you to customize your terminal colors, font settings, split panes and much more. You can read more about the different customizations [here](https://www.iterm2.com/features.html)

---

Install zsh

    brew install zsh

Install Oh-My-ZSH

    sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

- Open the `.zshrc` file via your favorite code editor

- Ensure source `$ZSH/oh-my-zsh.sh` is included in your file

- Add your favorite aliases in the file. Here are a few of my favorites:

      alias db='docker-compose build'
      alias l='ls -lah'
      alias ll='ls -lah'
      alias erc='cd ~/Code/erc'
      alias gs='git status'

- Save the file then run `source=~/.zshrc` in order for your terminal to recognize the changes

---

Install tmux

    brew install tmux

- tmux is a [terminal multiplexer](https://en.wikipedia.org/wiki/Terminal_multiplexer) that allows you to maintain persistant working state, while attaching and re-attaching to that session at will

* I currently have my [tmux.conf](https://gist.github.com/redsnow32/4127ed1b022339c4ee470151d9e73518) mapped to match the vim key-bindings

Install tmuxinator

    gem install tmuxinator

Copy over tmuxinator [auto-complete](https://github.com/tmuxinator/tmuxinator/blob/master/completion/tmuxinator.zsh)

Create a new config file for your project by running mux new `any name you want`

- This file gets saved as a .yml file in a `~/.tmuxinator directory`
- Edit the script via `mux edit "name you created above"`

* Here you're able to configure the layout of your terminal when firing up your app. You're able to fire up multiple instances within one session and work between each service

Run your project via `mux "name created above"`
