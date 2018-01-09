# Spicing up - My Dev Mac Machine 
Based over the orginal idea from [here](https://github.com/yrameshra0/mac-dev-setup). This is a comprehensive document that I could use to give myself a mental note about setting up _my garage (my mac)_ machine up for its endeavours.

Currently while preparing the document the High Sierra was the OS that I was working on.

1. First and formost on a vanilla mac, I have to have [Chrome](www.google.com/chrome). 
1. [iTerm](https://www.iterm2.com/version3.html) installation comes next.
1. Followed by [Homebrew](https://brew.sh/)
1. [Homebrew Cask](https://caskroom.github.io/) is too my favorite tool to pull down the process of installation and drag and drop game
1. Install [.dotfiles](https://github.com/Hacklor/dotfiles)

After the above steps now I'm ready to go ahead and put the nuts and bolts together of my mac machine

1. Install [jenv](http://www.jenv.be/) using ```brew install jenv```

jenv is used for handling multiple java jdks and easy management across them. Post installation don't forget to add the path related changes to profile.

At the time of writing this document `brew cask install java` bought `jdk9` and I want to have `jdk1.8` too hence follow below steps for making that happen

```brew tap caskroom/versions```

```brew cask install java8```

Post the command I want to add all the jdks to jenv using:

```jenv add /Library/Java/JavaVirtualMachines/<jdk version>/Content/Home```

Doing the above step for all the jdks available, I have to set a global jdk for usage:

```jenv global 1.8```

Post the above steps I want to enable plugins for jenv

```jenv enable-plugin export```

```jenv enable-plugin maven```

```jenv enable-plugin gradle```

```jenv enalbe-plugin scala```

```jenv enable-plugin springboot```