# My Raspberry Pi Setup
My raspberry Pi setup - self-hosting

<img src="./raspberrypi.webp" width="45%" alt="webp raspberry pi picture">

## Table of contents

- [My Raspberry Pi Setup](#my-raspberry-pi-setup)
  - [Table of contents](#table-of-contents)
  - [Main Sources](#main-sources)
  - [RBenv](#rbenv)
  - [Gollum](#gollum)
    - [B](#B)

## Main Sources

- [www.raspberrypi.com]([https://reactnative.dev/docs/environment-setup](https://www.raspberrypi.com/documentation/computers/getting-started.html#setting-up-your-raspberry-pi))

## RBenv
[source](https://dev.to/konyu/installing-the-latest-version-of-ruby-on-raspberry-pi-3ofk)
Rbenv is a version manager tool for the Ruby programming language on Unix-like systems

* RBenv Installation

```bash
sudo apt-get install rbenv
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> .bashrc
echo 'eval "$(rbenv init -)"' >> .bashrc

echo 'export GEM_HOME="$(ruby -e 'puts Gem.user_dir')"' >> .bashrc
echo 'export PATH="$PATH:$GEM_HOME/bin"' >> .bashrc
gem list
gem update
```

* Update your terminal

```
source .bashrc
```

* Test your installation

```
rbenv
> rbenv x.x.x #version to be displayed
```

## Gollum
[source](https://www.themoderncoder.com/install-and-configure-gollum-wiki-on-raspberry-pi/)

A Gollum Wiki is simply a git repository of a specific nature: A Gollum repository's contents are human-editable text or markup files.

* Gollum Installation
