# macOS For Development

Basic dev setup for macOS users

## Package Manager:

### [Homebrew](https://brew.sh/)

"Homebrew installs the stuff you need that Apple didn’t."

Homebrew formulae are simple Ruby scripts and Ruby comes pre-installed with macOS, you just need to paste this at a Terminal prompt to install Homebrew

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

You'll be using Homebrew or brew for most of the installations from now on.

***

## Version Control:

### [Git](http://git-scm.com/)

What's a developer without [Git](http://git-scm.com/)? To install, simply run:

    $ brew install git
    
When done, to test that it installed fine you can run:

    $ git --version
    
And `$ which git` should output `/usr/local/bin/git`.

Next, we'll define your Git user (should be the same name and email you use for [GitHub](https://github.com/) and [Heroku](http://www.heroku.com/)):

    $ git config --global user.name "Your Name Here"
    $ git config --global user.email "your_email@youremail.com"

They will get added to your `.gitconfig` file.

***

## Terminal:

### [iterm2](https://www.iterm2.com/)

"a replacement for Terminal and the successor to iTerm. It works on Macs with macOS 10.8 or newer. iTerm2 brings the terminal into the modern age with features you never knew you always wanted."

It is in many ways better than macOS Terminal, it provides featires like: Split Panes, built-in keyboard shortcut, etc.

<img alt="iterm2 Split Panes" src="https://www.iterm2.com/img/screenshots/split_panes.png">

To install iterm2 with brew, paste this at a Terminal prompt

```
brew cask install iterm2
```

***

### [Oh My Zsh](https://github.com/robbyrussell/oh-my-zsh) (Optional but highly recommended)

"Your terminal never felt this good before."

Zsh is an extended Bourne shell with a large number of improvements, including some features of Bash, ksh, and tcsh and Oh My Zsh is an open source, community-driven framework for managing your zsh configuration. Oh My Zsh comes with a shitload of plugins and themes to take advantage of. It comes pre-installed with some plugins which will make your Terminal look clutter-free, and lots of theme options, many of which display version-control data:

<img alt="Git Directory under Om My Zsh" src="https://git-scm.com/book/en/v2/images/zsh-oh-my.png">

To install Oh My Zsh, paste this at a Terminal prompt

```
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

***

## Node.js and NPM

### [Node.js](https://nodejs.org)

Node.js® — a version of Chrome’s V8 JavaScript runtime engine — which makes it possible to run JavaScript on the server-side.

Node.js is also used for deploying tools that make developing web sites simpler. For example, by installing Node.js on your desktop machine, you can quickly convert CoffeeScript to JavaScript, SASS to CSS, and shrink the size of your HTML, JavaScript and graphic files.

```
brew install node
```

When done, to test that it installed fine you can run:

```
node -v
```

***

### [NPM](https://npmjs.com)

NPM — a tool that makes installing and managing Node modules — it’s quite easy to add many useful tools to your web development toolkit.

npm is distributed with Node.js which means that when you intall Node.js, you automatically get npm installed on your computer. To see if NPM is installed, type `npm -v` in Terminal. This should print NPM’s version number so you’ll see something like this 5.6.0

```
npm -v
```

***

## Advanced setup

Setup for other environments like [Python](https://www.python.org), [C++](http://www.cplusplus.com) and [Ruby](https://www.ruby-lang.org).

[External link](https://sourabhbajaj.com/mac-setup) or it's [repo](https://github.com/sb2nov/mac-setup)
