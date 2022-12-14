# Create a repository change files commit and push to main

Using your git repository of choice, [Github](https://github.com/) for example.
1. Create new repository through web interface
2. Clone
3. Modify readme 
4. Commit with message
5. Push

## Create repository

There are 2 ways of creating a new repository on your git website:
> Got to your profile page, that would be https://github.com/[your-user-name-here]

1. Click on repositories tab then on new
2. At the top right of your page there is a **+** dropdown and there you can select new repository

*On repositories tab click new button*

![alt text](/docs/imgs/00-Create_from_repositories_tab.PNG "Create from repository's tab")


*Top right dropdown*

![alt text](/docs/imgs/01-Create_repo_from_profile_dropdown.png "Create from add drop down beside profile")

When done with either of the former:

1. Name your repository
2. Fill up your description
3. Choose if you want your repo public or private
4. Click on *Create repository*


*Create and name repository through web site*


![alt text](/docs/imgs/02-Create_and_name_your_repository.png "Create and name repository")

## Clone your repository

There are 2 ways to get your repository url:
1. Copy your repository base address
2. On the website, click Code makes sure you are on the Https tab and copy to clipboard

*Click Code makes sure you are on the Https tab and copy to clipboard*
![alt text](/docs/imgs/03-Get_repositories_url.png "Get repository url")

Now open up a command prompt on your computer, navigate to your favourite folder for storing source code and clone your repository. Your git clone command is typically
as follows

```
git clone [url-to-your-repo]
```

*Navigate to your source code folder and clone your repository*

![alt text](/docs/imgs/04-Clone_repository.png "Clone your repository")

## Commiting changes and pushing them

1. Navigate to your cloned repository folder
2. Change add text to README.md file
3. Run git status to see your modified files
4. Stage your modified files with the add command
5. Create a commit with a message
6. Push your commit to main

*Status, add staged files, create a commit with a message and push*

![alt text](/docs/imgs/05-git_staus_commit_push.PNG "Status, stage, commit with message and push")
