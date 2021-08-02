### Android Studio
```
# open from terminal
# add to ~/.bash_profile or ~/.zshenv
export PATH=$PATH:/Applications/Android\ Studio.app/Contents/MacOS/
export PATH=~/Library/Android/sdk/tools:$PATH
export PATH=~/Library/Android/sdk/platform-tools:$PATH
source ~/.bash_profile # source ~/.zshenv
```

### Adb
```
adb install ~/Downloads/file.apk
```

### BundleTool

```
# Generate release apk
./gradlew bundleRelease
brew install bundletool
bundletool.jar build-apks --bundle=nhl.aab --output=nhl.apks --overwrite --mode=universal
```
