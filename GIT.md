#### gitignore
 
When a file is added one time, git will keep track of it. 
Now if you add that file into `.gitignore`, git is expected to ignore that file.
However, because that file is already in the tracking list, so that file is not ignored.

In that case, you should remove the cache first then add all. 

```
git rm -r --cached .
git add .
git commit -m "file untracking changed"
```