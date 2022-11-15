# Make git ignore certain files

Most times when working, our tools generate files that are not central to our developent. That is that whenever another team member pick them they are useless for them, for example configuration files for Visual studio, Postman status files, etc.<br/>
Git has a certain type of file called .gitignore that store a set of rules for files that need to be ignored.

## Git ignore

Now execute the folowing steps:
1. Go to the root folder of you local repository
2. Look for .gitignore file (if it is not there, create a .gitignore file)
3. Edit your .gitignore file and add the rule from *Fig 1.0*

The following rule means that at any directory(```**/```) exclude the files ended with secrets.json(```*secrets.json```).
*Fig 1.0*
```
**/*secrets.json
```

## Creating secrets for your application

Lets make things intersting for git when ignoring files:

1. Create a *folder* called **Settings**, then *subfolder* called **Development**, then a *subfolder* called **Values** (this is to make it cumbersome for git to ignore a file)
2. Create a *file* called **mysuper.secrets.json** at *Settings/Development/Values*
3. Edit **mysuper.secrets.json** and your name and your birthday and save.
4. Stage, commit and push

After pushing you can go to your git web interface (i.e. www.github.com) and look at the file on your repo, *Settings/Development/Values/mysuper.secrets.json* shouln't be there.


