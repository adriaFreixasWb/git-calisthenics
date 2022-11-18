# Solving conflicts using an editor
On [session 3: managing-conflicts](/docs/Session3.md#managing-conflicts)
we saw a first way to deal with conflicts. To improve our experience, we are going to learn how to use a diff tool.

[Git diff](https://git-scm.com/docs/git-diff) is a way to see difference of a range of things, from two different files to two different branches. 
But what we mean by using a diff tool is to have a text editor equipped to handle the conflicts on a specific file. 
For our current session we will use [visual studio code](https://code.visualstudio.com/)

## Creating mulitple conflicts on the same file

From main branch, create a new file called list-of-conflicts.txt write the following on it

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
Have you ever gone sunbathing at the beatch
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
Now add the following changes to your *list-of-conflicts.txt*
```
Starting section
================
This is a start
Body
----
Your body is your best friend
Conclusion
----------
Handle your body with the upmost respect
The end
```
Now if you open *list-of-conflicts.txt* on visual studio code you will face something like this

![alt text](/docs/imgs/12-vs-code-diff-tool.PNG "Visual studio tool")

As you can see there are some familiar options, on top of <<<<<HEAD
- Accept current changes is equivalent to **git checkout --ours list-of-conflicts.txt**
- Accept Incoming changes is equivalent to **git checkout --theirs list-of-conflicts.txt**
- Accept both changes, this will simplty leave both version of the text on the same file
                                                                    
