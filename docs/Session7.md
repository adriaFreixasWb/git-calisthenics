# Untrack secret files to avoid having your passwords stored on your repository

## Upload an unwanted file to your repo by mistake

Create a file called **secrets.bymistake.txt** at the root of you repository, with some information in it
Stage, commit, push

## Uploaded file by mistake to my repository

On [the previous section](#Upload_an_unwanted_file_to_your_repo_by_mistake) we un added a file that didn't match our rule on .git ignore. 
And we pushed to our remote repository.
To fix that mistake wi will add another rule to cover this instance fore exampel add:
```
 **/secrets.*
```

Now stage, commit and push. Once pushed, got to your git web interface and check if the file is there.

## Untracking a file

