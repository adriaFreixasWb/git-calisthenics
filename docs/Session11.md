# Reverting commits

The revert command will create a commit that revers the changes of the commit being targeted. You can use it as follows (as seen on the previous section you need your commit hash)
```
git revert [commit to reveret]
```

This unlike the reset that we dido on the previous section, create a commit that undoes your previous changes and it stays on gits history for clarity.

## Working with Revert

Create a new branch as we practice called **feature/revert-commit**, then:
- Write *Something wrong* on README.md
- Commit your change
- Checkout main
- Merge **feature/revert-commit** into main
- Now look at your commit history with git log
- From git log take the commit hash that you want to undo.

For example if my last commit hash is **aa9dde082058288eb21ee05585c682cafaab10f3**
```
git revert aa9dde082058288eb21ee05585c682cafaab10f3
git push
```
Now if you go to your git web interface you can see you commit history and you will have to commits:
- something wrong
- revert "something wrong"

If you look into revert "something wrong" you will see that this commit just deletes everthing you have written on the something wrong commit.


