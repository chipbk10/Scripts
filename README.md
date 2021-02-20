# Scripts:

Other useful scripts

### Merge pdf files
```
pdfunite in_1.pdf in_2.pdf in_3.pdf out.pdf
```

### Run Visual Studio from terminal
```
# add in ~/.bash_profile

# visual studio
export PATH=$PATH:/Applications/Visual\ Studio\ Code.app/Contents/Resources/app/bin

source ~/.bash_profile

# now we can call
code folder
```

### Kill process
```
top                         # get a list of currently running process
ps aux | grep "name"        # a: show processes, u: show users, x: show processes not attached to terminal
ps aux | grep chrome

kill pID                    # pID: process ID
killall pName               # kill processes by name
kill -[1|2|9|15|17|19|23]   # 1: hangup, 2: interrupt from keyboard, 9: kill signal, 
                            # 15: terminate signal, 17, 19, 23: stop process
kill -9 2123
killall -9 chrome

```
### How to modify video's properties (resolution, frame rate)
```
ffmpeg -i input.mov -vf scale=886:1920 output.mov     # change resolution
ffmpeg -i input.mov -filter:v fps=30 output.mov       # change frame rate
```

### How to record simulator's screen
```
xcrun simctl io booted recordVideo --code=h264 --mask=black --force output.mov
```
