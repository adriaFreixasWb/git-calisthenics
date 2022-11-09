# Conflict resolution

Up to now it's been pretty straight forward, change source code, stage changes, commit, push, merge. What happens when we try to marge two branches and the changes create a conflict?

## Getting branches ready

In this instance we are going to emulate 2 different developers working at the same time.

Create a [new branch](Session2.md#Branching) called **feature/parallel-commit** but don't check it out yet.<br/>
Now make sure you are on main branch, do some changes on your README.md, stage them and commit.

Now [checkout](Session2.md#checkout-a-branch) feature/parallel-commit and make different changes to your README.md file, stage, commit and push them.

## Merging branches

To merge two different branches you need to be on the branch where you want add the changes to. Usually that would be main.

For example:
```
git checkout main
git merge feature/parallel-commit
```

## Managing conflicts

When merging if your changes go smoothly (no conflit) this is know as **fast-forward** merge.

On last section we tried to merge two branches: 
- feature/parallel-commit (that was one commit behind main)
- main that has changes on the same file as the merging branch

This scenario has been designed to result in a conflict. 
This situation is quiet usual:
- We create our branch from main
- A team mate makes a changes and merges his/hers barnchs to main 
- We work on the same file and we were unaware of the
- Our team mate's delta has a conflict with our delta
- We must solve the conflict fi we want to push to main


The simplest way to solve this conflict is to abort the current merge.
```
git merge --abort
```

Now switch branches again to feature/parallel-commit and merge main into your current branch
```
git checkout feature/parallel-commit
git merge main
```
You now have a **conflict on your branch** which is **safer than** to have a **conflict in main**.

Since we have pushed our changes to our current branch (feature/parallel-commit), we can accept all changes comming from main to solve our conflicts.
```
git checkout --theirs README.md
git add README.md
git commit -m "merge conflicts solved"
```

> Watch out because now main will have overriden your changes and you need to redo them again. <br/>
> You can go to your git web interface, find your last commit and copy it again on README.md

Now you had a fast forward merge so you can go back to:
1. checkout main 
2. merge feature/parallel-commit
3. push 

And can [delete your old branch](Session2.md#delete-an-old-branch)

