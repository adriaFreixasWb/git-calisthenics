# Git history

How to rename a branch. The easiest way to rename a branch is:
- Create and checkout branch from your current branch
- [Set upstream](docs/Session2.md#checkout-a-branch) for your newly creatd branch
- [Delete your original local](Session2.md#delete-an-old-branch) branch

```
git push origin --delete [your-original-branch-name]
```

Now checkout your newly created branch and everything is back to normal
And you have your new branch
