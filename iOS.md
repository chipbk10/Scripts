### CocoaPods:
```
sudo gem install cocoapods
pod init
pod install
pod update
open project.xcworkspace
```

### XCRUN
```
xcrun simctl erase all                                    # to erase and reset all simulators
xcrun simctl erase F3-3ED6-4E10-                          # to erase and reset a simulator
xcrun simctl shutdown all                                 # to shutdown all simulators
xcrun simctl shutdown F3-3ED6-4E10-                       # to shutdown a simulator

xcrun instruments -s                                      # list all devices
xcrun instruments -w F3-3ED6-4E10- -t Blank               # to run any simulator by GUID:
xcrun simctl install booted /path/to/your.app             # to install app to the booted simulator
xcrun simctl uninstall booted /path/to/your.app           # to remove app from the booted simulator
xcrun simctl launch booted "com.app.bundleIdentifier"     # to launch the app in the booted simulator
                                                          # "com.app.bundleIdentifier" is your CFBundleIdentifier in Info.plist
```
