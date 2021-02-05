### Android Studio
```
# open from terminal
# add to ~/.bash_profile
export PATH=$PATH:/Applications/Android\ Studio.app/Contents/MacOS/
source ~/.bash_profile
```

### BundleTool

```
# Generate release apk
./gradlew bundleRelease
brew install bundletool
bundletool.jar build-apks --bundle=nhl.aab --output=nhl.apks --overwrite --mode=universal
```
