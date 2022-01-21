# Mac Setup For PHP
## Install Homebrew
Homebrew is a dependency manager for your OS and it makes it a ton easier to install development packages and/or change versions of bundled packages that come with your OS (e.g. PHP version).
You can install Homebrew with the following command:
```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```
## Install Composer, Git & PHP
Now that we have Homebrew, we can accelerate the install of packages by grouping them together. For instance, let’s install Composer, Git, and PHP!
```sh
brew install php git composer
```
Note that this process will install the most current version of PHP (for me in 2021 this was PHP 8.0). Once the install completes, you can immediately run php, composer, and git commands from a new terminal session. This is another huge benefit of using Homebrew (it just works).
You can manually tweak the specific version of PHP by running a Homebrew command like:
```sh
brew install php@7.4
```
This will pull down the necessary dependencies and the package for this explicit version of PHP. I can then swap out my installed version of PHP
```sh
brew unlink php 
brew link php@7.4 --force
```
## Install Mysql Version 5.7
Install Mysql@5.7 via homebrew
```sh
brew install mysql@5.7
```
