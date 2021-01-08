### Ruby:

```
curl -L https://get.rvm.io | bash -s stable # download and install a stable version of rvm (ruby packages manager)
rvm install ruby-3.0.0
source /Users/UserName/.rvm/scripts/rvm     # activate rvm
rvm docs generate-ri                        # install ruby documents
```

### Node:

Install, and activate node
```
brew install node
brew info node                    # see info about node (version, dependencies)
npm root -g                       # shows the directory the global modules are installed in
add the path to ~/.bash_profile
source ~/.bash_profile            # activate paths
```

How to completely uninstall node?
```
brew uninstall node
brew uninstall --force node
brew uninstall --ignore-dependencies node
brew uninstall --ignore-dependencies node icu4c

sudo rm -rf /opt/local/bin/node /opt/local/include/node /opt/local/lib/node_modules
sudo rm -rf /usr/local/bin/npm /usr/local/share/man/man1/node.1 /usr/local/lib/dtrace/node.d
rm -rf /Users/[homedir]/.npm
rm -rf /Users/[homedir]/.nvm

brew doctor                       # check all broken links
brew missing
brew cleanup --prune-prefix       # remove all broken links
```

### NPM

```
sudo npm install[i] -g package    # install a package globally
sudo npm uninstall[i] -g package  # uninstall a package globally
npm list                          # list all installed packages
npm root -g                       # shows the directory the global modules are installed in
```
