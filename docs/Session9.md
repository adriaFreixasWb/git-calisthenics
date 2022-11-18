## Moving git's HEAD 

As we saw at [last section of the former Session](Session8.md#what-is-a-gits-head)
HEAD is where de repository is pointing at. **(HEAD -> main** means that our local head is up to date with all commit at main branch.

As we said *git’s version control model is based on snapshots*, therefore we could move the HEAD to any commit we want.<br/>
Just as we checkout branches, or files (remember solving confilts section? *git checkout README.md --theirs*) we can checkout commits.<br/>
To checkout a commit use the following command
```
git commit [commits-has-humber]
```

For example, if I take the hush of the previous commit (62e5df7a6d2934f477ec644ad365a07cc6b94e6d) and go
```
git checkout 62e5df7a6d2934f477ec644ad365a07cc6b94e6d
```
Now I get:
```
$ git checkout 62e5df7a6d2934f477ec644ad365a07cc6b94e6d
Note: switching to '62e5df7a6d2934f477ec644ad365a07cc6b94e6d'.

You are in 'detached HEAD' state. You can look around, make experimental 
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.      

If you want to create a new branch to retain commits you create, you may 
do so (now or later) by using -c with the switch command. Example:       

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 62e5df7 Corrent mistake
M       docs/Session8.md
```

Meaning that I have my HEAD on a commit that is not consistent with any branch (enche detached). And that we are back at our previous commit that has changes only on docs/Session8.md.

To leave this state as the text says execute
```
git switch -
```

And you would be back to main.
