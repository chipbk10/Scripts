# Scripts

### Merge pdf files
```
pdfunite in_1.pdf in_2.pdf in_3.pdf out.pdf
```
### SSH key
```
ssh-keygen -t [algorithm] -b [fileSize] `generate ssh private & public keys`
ssh-keygen -t rsa -b 4096
pbcopy < ~/.ssh/id_rsa.pub # copy ssh public key

ssh-agent -s # using SSH-AGENT to manage private key, and communicate with server -> No need to enter passphrase all the time
ssh-add ~/.ssh/id_rsa # add private key into ssh-agent
ssh-add -l # list all private keys in ssh-agent
```
### Ruby:
```
curl -L https://get.rvm.io | bash -s stable # download and install a stable version of rvm (ruby packages manager)
rvm install ruby-3.0.0
source /Users/linhpham/.rvm/scripts/rvm # activate rvm
rvm docs generate-ri # install ruby documents
```

