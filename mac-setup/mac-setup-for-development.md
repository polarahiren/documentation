# Mac Setup For Development
## Installing Iterm
Visit [this](https://iterm2.com/downloads.html) link to download Iterm on our Mac system.
## Installing oh-my-zsh
Oh My Zsh is an open source, community-driven framework for managing your zsh configuration.
​
Sounds boring. Let's try again.
​
Oh My Zsh will not make you a 10x developer...but you may feel like one.
​
Once installed, your terminal shell will become the talk of the town or your money back! With each keystroke in your command prompt, you'll take advantage of the hundreds of powerful plugins and beautiful themes. Strangers will come up to you in cafés and ask you, "that is amazing! are you some sort of genius?"
​
Finally, you'll begin to get the sort of attention that you have always felt you deserved. ...or maybe you'll use the time that you're saving to start flossing more often. 😬
​
It can be install by CURL using below command
​
```sh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
​
## Instaling PHPstorm
​
PHPstorm is a powerful IDE to ease your approach to code. PHPstorm can be available on [this](https://www.jetbrains.com/phpstorm/nextversion/) Link.
​
You can customize your preference accordingly in preferance setting of PHPstorm. Preference such as theme, text size, line height, plugins, key map and much more
​
## Installing node, NPM and Yarn
### Installing Node
Node can be installed on your mac from [this](https://nodejs.org/en/) link. Donwanload Node from given link and install it in your mac.
​
### Installing yarn
It is recommended to install Yarn through the npm package manager, which comes bundled with Node.js when you install it on your system.
​
Once you have npm installed you can run the following both to install and upgrade Yarn:
​
```sh
npm install --global yarn
```
​
## Install Homebrew
​
Homebrew is a dependency manager for your OS and it makes it a ton easier to install development packages and/or change versions of bundled packages that come with your OS (e.g. PHP version).
​
You can install Homebrew with the following command:
​
```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```
​
​
## Install Composer, Git & PHP
​
Now that we have Homebrew, we can accelerate the install of packages by grouping them together. For instance, let’s install Composer, Git, and PHP!
​
```sh
brew install php git composer
```
​
Note that this process will install the most current version of PHP (for me in 2021 this was PHP 8.0). Once the install completes, you can immediately run php, composer, and git commands from a new terminal session. This is another huge benefit of using Homebrew (it just works).
​
You can manually tweak the specific version of PHP by running a Homebrew command like:
​
```sh
brew install php@7.3
```
​
This will pull down the necessary dependencies and the package for this explicit version of PHP. I can then swap out my installed version of PHP
​
```sh
brew unlink php 
brew link php@7.3 --force
```
​
## Install Mysql Version 5.7
​
Install Mysql@5.7 via homebrew
​
```sh
brew install mysql@5.7
```
## Setting Up Laravel valet
​
Valet is a Laravel development environment for macOS minimalists. Laravel Valet configures your Mac to always run Nginx in the background when your machine starts. Then, using DnsMasq, Valet proxies all requests on the *.test domain to point to sites installed on your local machine.
​
In other words, Valet is a blazing fast Laravel development environment that uses roughly 7 MB of RAM. Valet isn't a complete replacement for Sail or Homestead, but provides a great alternative if you want flexible basics, prefer extreme speed, or are working on a machine with a limited amount of RAM.
​
you should make sure the ~/.composer/vendor/bin directory is in your system's "PATH". you may install Laravel Valet as a global Composer package:
​
```sh
composer global require laravel/valet
```
​
Finally, you may execute Valet's install command. This will configure and install Valet and DnsMasq. In addition, the daemons Valet depends on will be configured to launch when your system starts:
​
```sh
valet install
```
## Installing SequelPro
​
Sequel pro (mysql client) can be downloaded from [this](https://www.sequelpro.com/) link and database can be accessed from it.