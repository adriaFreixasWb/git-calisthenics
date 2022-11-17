# Undo your last commit

Sometime your realize that you just pushed a wrong commit to your main branch and want to turn back the wheels of time.<br/>
One of many ways to do it is to reset your head back one commit and create a new branch.

## Preparaing te scenario

We are going to pretend that we did a mistake, so on **main** branch, edit your **README.md** and add somewhere
```
Some wrong doing
```
Now save, stage, commit, push, and check that on your git web interface that you have these last changes

## Reset

We need to go one step back in our commit history to that end we are going to use the reset command. Since we only one to go back one commit we don't need any guids.<br/>
To go back just one commit
```
git reset HEAD^
```

Apparenly nothing happened, but if you execute a **git status command** you will see that your *README.md* file has been modified so to get it to its previous state 
```
git restore README.md
```

Now your file does not contain your last pushed changes anymore, if you execute a **git status command** again you will be told that you are behind origin/main by one commit.<br/>
Now we are right were we wanted, so we will create a new branch:
```
git checkout -b bugfix/delete-last-commit

```
We created and checkout a branch called bugfix/delete-last-commit if you execute a **git status command** again you will get 
```
On branch bugfix/delete-last-commit
nothing to commit, working tree clean
```

Now we can edit our *README.md* file and add
```
Everything is back to normal.
```

Now save, stage, commit and push.<br/>
Now comes the tricky part so pay attention, you must:
1. Checkout main
2. Pull main to get back the first wrong changes we did to main 
3. Checkback bugfix/delete-last-commit
4. Merge main into bugfix/delete-last-commit

```
git checkout main
git pull
git checkout bugfix/delete-last-commit
git merge main
```

Now of course we have a conflict, because main is ahead of our current branch by one commit. If you execute a **git status command** again you will see that the conflict is at *README.md*. So, we will do the reverse of what we did at our first [Conflict resolution](Session3.md#managing-conflicts)

```
git checkout README.md --ours
```
Now our changes have overriten the ones from master and we have solve the conflict. Now we need to:
1. Save,  stage, commit, pus
2. checkout main
3. merge bugfix/delete-last-commit into main
4. we will get a Fast-forwar message
5. git push

Now checkout at your git web interface that all your new change are stored at main and you are golden.

## resset many commits

To go back 2 commits 
```
git reset --hard HEAD~2
```

To go back 3 commits
```
git reset --hard HEAD~3
```

To go back to as pecific commit (you need to know the hash)
```
git reset --hard <hash>
```