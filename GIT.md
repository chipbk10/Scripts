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

### SSH key

```
ssh-keygen -t [algorithm] -b [fileSize] # generate ssh private & public keys
ssh-keygen -t rsa -b 4096
pbcopy < ~/.ssh/id_rsa.pub              # copy ssh public key

ssh-agent -s          # using SSH-AGENT to manage private key, and communicate with server -> No need to enter passphrase all the time
ssh-add ~/.ssh/id_rsa # add private key into ssh-agent
ssh-add -l            # list all private keys in ssh-agent
```
