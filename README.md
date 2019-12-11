# Brodie's dotfiles

![Screenshot.png](Screenshot.png)

## Bash

1. [Download GitHub for macOS](https://central.github.com/deployments/desktop/desktop/latest/darwin)
1. [Clone this repo](x-github-client://openRepo/https://github.com/brod-ie/dotfiles) into `~/GitHub/`
1. `cd ~ && ln -s ~/GitHub/dotfiles/bash/.bash_profile . && ln -s ~/GitHub/dotfiles/bash/.hushlogin .`

## macOS

1. `dotfiles && ./macos/macosh.sh`

## Homebrew

1. `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
1. `brew cask install brooklyn`

## SSH Config

1. `cd ~/.ssh && ln -s ~/GitHub/dotfiles/ssh/config .` (N.B. for obvious reasons, this doesn't live here, nor do certs)

## Sublime Text

1. Ensure that the `subl` folder in iCloud Drive is downloaded
1. [Download Sublime](https://www.sublimetext.com/3)
1. `cd ~/Library/Application\ Support/Sublime\ Text\ 3/Packages && rm -rf User && ln -s ~/Library/Mobile\ Documents/com~apple~CloudDocs/subl/User`

## NGINX and PHP

1. `brew install nginx && brew install php70`
1. `cd /usr/local/etc/nginx/ && rm -rf nginx.conf && ln -s ~/GitHub/dotfiles/nginx/nginx.conf .`
1. `cd /usr/local/etc/nginx/ && rm -rf servers && ln -s ~/GitHub/dotfiles/nginx/servers/ .`
1. `cd /usr/local/etc/nginx/ && ln -s ~/GitHub/dotfiles/nginx/include/ .`
1. `cd /usr/local/etc/php/7.2/php-fpm.d/ && rm -rf www.conf && ln -s ~/GitHub/dotfiles/php/www.conf .`
1. `sudo brew services restart nginx && sudo brew services start php70`

## Xcode

1. `cd ~/Library/Developer/Xcode/UserData && rm -rf CodeSnippets && rm -rf FontAndColorThemes && rm -rf KeyBindings && ln -s ~/GitHub/dotfiles/xcode/CodeSnippets . && ln -s ~/GitHub/dotfiles/xcode/FontAndColorThemes . && ln -s ~/GitHub/dotfiles/xcode/KeyBindings .`
