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

# How to extract apk files from aab
# https://www.geekdashboard.com/extract-apk-files-from-aab/
java -jar bundletool.jar build-apks --bundle=nhl.aab --output=nhl.apks --overwrite --mode=universal
```
