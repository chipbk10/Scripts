### Using ReactNative
```
npx react-native init project

npm install library [--save]
npm list                              # list all dependencies of project
npm start                             # run a node project

npx react-native run-ios
npx react-native install-ios
npx pod-install

npx react-native start --reset-cache  # Reset metro bundler cache
cd android && ./gradlew clean         # Remove Android assets cache
npx react-native run-android
touch local.properties
# add in local.properties: 
# sdk.dir = /Users/chipbk10/Library/Android/sdk
```


### Using Expo

```
sudo npm i -g expo-cli
npm root -g                           # shows the directory the global modules are installed in
edit & add path to ~/.bash_profile    
source ~/.bash_profile

expo HelloWorld
cd HelloWorld
npm start

```
