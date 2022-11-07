# Conflict resolution

Up to now it's been pretty straight forward, change source code, stage changes, commit, push, merge. What happens when we try to marge two branches and the changes is not fast-forward?

## Getting branches ready

In this instance we are going to emulate 2 different developers working at the same time.

Create a [new branch](Session2.md#Branching) called **feature/parallel-commit** but don't check it out yet.
Now make sure you are on main branch, do some changes on your README.md, stage them and commit.

Now [checkout](Session2.md#checkout-a-branch) feature/parallel-commit and make different changes to your README.md file, stage, commit and push them.

## Merging branches

To marge two different branches you need to be on the branch where you want add the changes to. Usually that would be main.

For example:
```
git checkout main
git merge feature/parallel-commit
```

## Managing conflicts

When merging if your changes go smoothly (no conflit) this is know as **fast-forward** merge.

On last section we tried to merge a two branches: 
- feature/parallel-commit (that was one commit behind main)
- main that has changes on the same file as the merging branch

The simplest way to solve this conflict is to reset your main branch.
```
git reset 
```
With git status you will get your pending changes, this will tell you that you can restore your README to its original state.
```
git restore README.md
```
Now switch branches again to feature/parallel-commit and merge master into your current branch
```
git checkout feature/parallel-commit
git merge main
```

> Whatch out because now master will have overriden your changes and you need to redo them again.

Now you had a fast forward merge so you can go back to:
1. checkout main 
2. merge feature/parallel-commit
3. push 

And can [delete your old branch](Session2.md#delete-an-old-branch)

