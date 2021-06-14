# Scripts:

Other useful scripts

### Merge & Separate pdf files
```
pdfunite in_1.pdf in_2.pdf in_3.pdf out.pdf
pdfseparate input.pdf %d.pdf
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
ffmpeg -i input.mov -vf scale=886:1920 output.mov                     # change resolution
ffmpeg -i input.mov -vf scale=886:1920,setsar=1:1 output.mov          # change resolution (better)
ffmpeg -i input.mov -filter:v fps=30 output.mov                       # change frame rate
ffmpeg -i input.jpg -vf scale=320:240 output_320x240.png              # same works for image too
```

### How to record simulator's screen
```
xcrun simctl io booted recordVideo --code=h264 --mask=black --force output.mov    # no sound --> Apple will reject

# using iMovie to combine audio & video
# choose File -> New App Preview. First import (CMD+I) the screen shot, 
# and then the video you recorded. This way the exported video will be the proper resolution.

```

### How to know size of a folder
```
du -sh folder
du -sh *                                        # display sizes of all folders & files in the current folder
du -sh * | sort -rh                             # display & sort by decreasing order
du -sh * | sort -rh | head -20                  # display top-20 biggest sub-folders in the current folder
```
