# Solving conflicts using a diff tool

On [session 3: managing-conflicts](/docs/Session3.md#managing-conflicts)
we saw a first way to deal with conflicts. To improve our experience, we are going to learn how to use a diff tool.

[Git diff](https://git-scm.com/docs/git-diff) is a way to see difference of a range of things, from two different files to two different branches. 
But what we mean by using a diff tool is to have a text editor equipped to handle the conflicts on a specific file. 
For our current session we will use [visual studio code](https://code.visualstudio.com/)

## Creating mulitple conflicts on the same file

From main branch, create a new file called list-of-conflicts.txt writte the follwing on it

```
Starting section
----------------
Introduction
------------
Body
----
Conclusion
----------
The end
-------
```

Now follow this steps
- Stage, commit and push it.
- Create and new branch called feature/multi-conflict
- Add the follwing modifications to list-of-conflicts.txt

```
Starting section
----------------
The sun is a start
Introduction
------------
Have you ever gone sunbathing at the bitch
Body
----
Summer is nice and a time for the outdoors
Conclusion
----------
You can get burned by the sun so use sun screen
The end
-------
I hope this is everything you hopped for
```

Now checkout main, you will see once again that the changes made on your branch are not on main.<br/>
Now add the folowing chanes to your list-of-conflicts.txt
```
Starting section
================
This is a start
Body
----
Your boady is your best friend
Conclusion
----------
Handle your body with the upmost respecte
The end
```



