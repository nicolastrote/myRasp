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

### Gollum Installation

For building Gollum we need:

```
apt-get install ruby ruby-dev make zlib1g-dev libicu-dev build-essential git cmake
```
Now it time to install gollum:

```
gem install gollum --user-install
```

### Git Connexion

Gollum uses a git repo as its backend.

In order to fix the issue follow the below steps:

* Goto settings of Github account
* Find and Select Developer Settings
* Find and Select Personal access tokens
* Generate a new token
* Fill in any note and select the access scopes
* once done click on generate token
  * personal aceess token
  * read & write only on "Content"
  * keep your token in safe: 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
* Use the generated token in place of a password to communicate with GitHub

```
git clone https://github.com/nicolastrote/myGollumWiki.git
```

### Running Gollum as a service

```
gollum /home/nicolas/myGollumWiki/ --css
```

