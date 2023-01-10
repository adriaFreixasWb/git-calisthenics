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
- Checkout maing
- Merge **feature/revert-commit**
- Now look at your commit history with git log
- From git log take the commit has that you want to undo.
