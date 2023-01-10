# Untrack secret files to avoid having your passwords stored on your repository

## Upload an unwanted file to your repo by mistake

Create a file called **secrets.bymistake.txt** at the root of you repository, with some information in it
Stage, commit, push

## Uploaded file by mistake to my repository

On [the previous section](#Upload_an_unwanted_file_to_your_repo_by_mistake) we un added a file that didn't match our rule on .git ignore. 
And we pushed to our remote repository.
To fix that mistake wi will add another rule to cover this instance fore exampel add:
```
 secrets.*
```

Now stage, commit and push. Once pushed, go to your git web interface and check if the file is there.

## Untracking a file

Oops after adding our new rule, our file is till there. On a real enviroment this could cause some stress. Don't worry, there is an easy fix for that.<br/>
As we have been doing all along we need to (stage) track a file before we can commit it to our local repository. That is what we do when we execute:
```
git add .
```
The period(.) at the end means everything, we could also have specified a file name after the add command.<br/>

If there is an add command, you guessed it, there is also a remove command (rm). But be carefule because git rm secrets.bymistake.txt will delete the file so instead:
```
git rm -r --cached secrets.bymistake.txt
git commit -a -m "Remove secrets files"
```

Now that we had it removed we no longer need to worry because the .git ignore will do its job.
