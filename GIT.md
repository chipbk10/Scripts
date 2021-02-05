### Gitignore
 
When a file is added one time, git will keep track of it. 
Now if you add that file into `.gitignore`, git is expected to ignore that file.
However, because that file is already in the tracking list, so that file is not ignored.

In that case, you should remove the cache first then add all. 

```
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

### Working with multiple repositories

```
# fetch all of the remote branches
git fetch remote_name
git fetch origin

# check all branches of all remotes
git branch -av

# checkout a specific branch of a remote
git checkout -b branch_name remote_name/branch_name
git checkout -b master origin/master

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
