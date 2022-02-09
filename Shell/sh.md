- Check if a variable has value or not
```
if [ -z $variable]; then
  echo "Error: variable is not provided"
  exit 1
else
  echo "Success: variable = $variable"
fi
```
- Read parameters from user
```
while :
do
  echo "Please enter parameter1 ?"
  read parameter1
  echo [$parameter1]
  
  echo "Please enter parameter2 ?"
  read parameter2
  echo [$parameter1]-[$parameter2]
  
  echo "All parameters are correct? y/n"
  read isCorrect
  if [[ $isCorrect == y* ]]; then
    break
  fi
done
```
- let user choose an option in a list
```
options = "Option1 Option2 Option3 Custom"
echo "Please select an option for the change?"
select option in $options
do
  if [ $option == "Custom" ]; then
    echo "Please type your custom option"
    read option
  fi
done
```
- Create a folder if it doesn't exist
```
  folder = "MY_FOLDER"
  if [ ! -d $folder ]; then
    mkdir $folder
  fi
```

- Todo: bump_app_version, generate_changelog_upcoming, localise_download
