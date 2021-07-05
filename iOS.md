### CocoaPods:
```
# how to completely remove cocoapods:
sudo gem uninstall cocoapods
sudo gem uninstall cocoapods-core
sudo gem uninstall cocoapods-downloader

# install
sudo gem install cocoapods

# run
pod init
pod install
pod install --repo-update                                 # to be sure you get the latest version
pod update
open project.xcworkspace

# remove pods from project
sudo gem install cocoapods-deintegrate cocoapods-clean
pod deintegrate
pod cache clean --all
rm -rf Pod* Project.xcworkspace
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

### Carthage

````
touch Cartfile                                            # create Carthage file, then add dependencies
Cartfile.resolved                                         # this file contains info about versions of the dependencies, should be stored in the repository
````

#### Carthage directory
- Build 		# built frameworks
- Checkouts 	# source code

#### Notes
- Carthage maintains its own internal cache (database) of dependency repositories, 
- so it doesn’t have to clone the same source multiple times for different projects.

````
carthage update                                           # clone the repositories (dependencies), then build each dependency into a framework
carthage update --platform iOS
carthage bootstrap --no-build                             # Carthage skip download the binary builds
````

#### bootstrap vs update
````
carthage bootstrap 					  # checkout & build
carthage update 					  # update & re-build
````
