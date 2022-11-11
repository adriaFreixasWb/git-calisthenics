# Rename your branch

How to rename a branch. The easiest way to rename a branch is:
- Create and checkout branch from your current branch
- [Set upstream](Session2.md#checkout-a-branch) for your newly creatd branch
- [Delete your original local](Session2.md#delete-an-old-branch) branch

```
git push origin --delete [your-original-branch-name]
```

Now checkout your newly created branch and everything is back to normal<br/>
[Here you have a full explanation](https://www.ionos.com/digitalguide/websites/web-development/renaming-a-git-branch/#:~:text=To%20do%20this%2C%20use%20the%20following%20steps%3A,git%20branch%20%2Da%E2%80%9D%20command.) on how to rename your branches 
