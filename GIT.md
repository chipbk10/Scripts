### Gitignore
 
When a file is added one time, git will keep track of it. 
Now if you add that file into `.gitignore`, git is expected to ignore that file.
However, because that file is already in the tracking list, so that file is not ignored.

In that case, you should remove the cache first then add all. 

```
# delete all existing .DS_Store files in the repository
find . -name .DS_Store | xargs -0 rm

# clear the cache
git rm -r --cached .
git add .
git commit -m "file untracking changed"
```

### Steps to clear out the history

```
# remove the history from 
rm -rf .git      

# recreate the repos from the current content only
git init
git add .
git commit -m "Initial commit"

# push to the github remote repos ensuring you overwrite history
git remote add origin git@github.com:<YOUR ACCOUNT>/<YOUR REPOS>.git
git push -u --force origin master
```

### GitConfig
```
# global git config
cat ~/.gitconfig

# local git config or inside a git repository folder
cat /usr/local/etc/gitconfig

# Xcode git config
sudo vim /Applications/Xcode_13_2_1.app/Contents/Developer/usr/share/git-core/gitconfig

git config --global user.email
git config --local user.email "someone@gmail.com"

# credential.helper: you will be asked for a username and password, and they will be saved in ~/.git-credentials file
git config --global credential.helper store

# credential.helper: osxkeychain
git config --global credential.helper osxkeychain

```
### Working with multiple repositories

```
# shows all the branches on the remote, including those that are not tracked locally 
# and even those that have not yet been fetched
git remote show remote_name

# fetch all of the remote branches
git fetch remote_name
git fetch origin

# fetch && delete obsolete remote-tracking branches
git fetch origin --prune

# fetch and update all remotes
git remote update --prune

# check all branches of all remotes
git branch -av

# checkout a specific branch of a remote
git checkout -b branch_name remote_name/branch_name
git checkout -b master origin/master

# rename an existing git remote
git remote rename origin devoteam

```

### Working with branches

```
# delete a local branch
git branch -d branch_name
git branch -D branch_name           # -D = -d --force

# delete a remote branch
git push -d remote_name branch_name
git push -d origin dev              # delete the branch called dev from remote origin

# branch out from a branch
git checkout -b dev master          # create a local branch called dev from local master
git checkout -b dev origin/master   # create a local branch called dev from remote master
git checkout dev                    # switch to dev

# push to a remote branch with different name
git push -u remote_name local_branch_name:remote_branch_name
git push -u origin dev:master

# set tracking information for the local branch
git branch --set-upstream-to=origin/master master   # point local master to remote master

```

### Git merge vs git rebase
```
git checkout master
git merge feature                   # merge all changes from feature into master in 1 commit
                                    # we don't care whatever changed (commits) in feature
git rebase feature                  # merge all changes from feature into master, and preserve all commits from feature
                                    # rewrite the history of commits, arrange them by time
```

### SSH key

```
ssh-keygen -t [algorithm] -b [fileSize] # generate ssh private & public keys
ssh-keygen -t rsa -b 4096
pbcopy < ~/.ssh/id_rsa.pub              # copy ssh public key

ssh-agent -s          # using SSH-AGENT to manage private key, and communicate with server -> No need to enter passphrase all the time
ssh-add ~/.ssh/id_rsa # add private key into ssh-agent
ssh-add -l            # list all private keys in ssh-agent
```

### Https
- to store `git credential` we can use `keychain`. Add new `password item`, fill `username`, `password`, allow application `iterm` to access
