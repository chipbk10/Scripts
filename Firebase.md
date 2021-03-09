### Firebase CLI
```
mkdir firebase                  # create local firebase directory
cd firebase

npm install -g firebase-tools   # install firebase cli in the current directory
bin/firebase login              # login into firebase

# Or we can add the path bin/firebase to .bash_profile for convenience
npm get prefix                  # get the root directory
vim ~/.bash_profile
export "root_directory/bin:$PATH"
```

### Publish app-ads.txt with Firebase Hosting
```
firebase init                   # initialize your firebase project in your local machine
                                # select to set up Hosting
                                # use an existing project
                                # specify a directory to use as your public root directory. Default (public)
                                # since the website you're going to create is not a single-page app, select N

cd public                       # Put the app-ads.txt file into the public directory in your local project directory.
touch app-ads.txt
echo "code snippet ..." >> app-ads.txt
firebase deploy --only hosting  # publish to firebase hosting server
                                # verify by visiting website : https://PROJECT_ID.web.app/app-ads.txt
                                # in app store connect: update the developer website with the link https://PROJECT_ID.web.app
                                # redirect to your website by adding url_to_redirect in firebase.json
                                # source: https://developers.google.com/admob/android/app-ads#firebase
```
