# Scripts

### Merge pdf files
```
pdfunite in_1.pdf in_2.pdf in_3.pdf out.pdf
```
### SSH key
```
ssh-keygen -t [algorithm] -b [fileSize]
ssh-keygen -t rsa -b 4096
pbcopy < ~/.ssh/id_rsa.pub
```
#### Using SSH-AGENT to manage private key, and communicate with server -> No need to enter passphrase all the time
```
ssh-agent -s
ssh-add ~/.ssh/id_rsa
ssh-add -l
```
