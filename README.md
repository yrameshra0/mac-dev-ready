# Spicing up - My Dev Mac Machine 
Based over the orginal idea from [here](https://github.com/yrameshra0/mac-dev-setup). This is a comprehensive document that I could use to give myself a mental note about setting up _my garage (my mac)_ machine up for its endeavours.

Currently while preparing the document the High Sierra was the OS that I was working on.

1. First and formost on a vanilla mac, I have to have [Chrome](www.google.com/chrome). 
1. [iTerm](https://www.iterm2.com/version3.html) installation comes next.
1. Followed by [Homebrew](https://brew.sh/)
1. [Homebrew Cask](https://caskroom.github.io/) is too my favorite tool to pull down the process of installation and drag and drop game
1. Install [.dotfiles](https://github.com/Hacklor/dotfiles).
   Mental note remember to configure the iterm preferences and post that properly setting `zsh` as a login shell using steps shown [here](https://apple.stackexchange.com/questions/88278/change-default-shell-from-bash-to-zsh/88296#88296)
1. Install CleanMyMac using `brew cask install cleanmymac`

After the above steps now I'm ready to go ahead and put the nuts and bolts together of my mac machine

1. Install [jenv](http://www.jenv.be/) using ```brew install jenv```

   jenv is used for handling multiple java jdks and easy management across them. Post installation don't forget to add the path related changes to profile.

   At the time of writing this document `brew cask install java` bought `jdk9` and I want to have `jdk1.8` too hence follow below steps for making that happen

   ```
   brew tap caskroom/versions
   brew cask install java8
   ```

   Post the command I want to add all the jdks to jenv using: 

   `jenv add /Library/Java/JavaVirtualMachines/<jdk version>/Content/Home`

   Doing the above step for all the jdks available, I have to set a global jdk for usage use `jenv global 1.8`

   Post the above steps I want to enable plugins for jenv

   ```
   jenv enable-plugin export
   jenv enable-plugin maven
   jenv enable-plugin gradle
   jenv enable-plugin scala
   jenv enable-plugin springboot
   ```
1. Install IntelliJ-Idea using `brew cask install intellij-idea`
1. Install Visual Studio Code using `brew cask install visual-studio-code`
1. Install Docker-CE using `brew cask install docker`
1. Install VirtualBox using `brew cask install virtualbox`
1. Install Node by following steps [here](http://nodesource.com/blog/installing-node-js-tutorial-using-nvm-on-mac-os-x-and-ubuntu/).

   I like to install `node` using `nvm` for similar reason why I installed `jenv` above for `java`. `Nvm` help managing multiple versions of node with ease.
1. Install AWS-Cli using `brew install aws-cli`
1. Install Ansible using `brew install ansible`
1. Install Terraform using `brew install terraform`

