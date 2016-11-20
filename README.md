# Git
## Create a new repository on the command line

init repository in local folder
```Shell
git init
```

add or track file
```Shell
git add README.md
```

commit changes and add message
```Shell
git commit -m "first commit"
```

add remote repository with the name origin
```Shell
git remote add origin git@github.com:LiqiLearningGroup/Git.git
```

push commits
```Shell
git push -u origin master
```

just push an existing repository from the command line
```Shell
git remote add origin git@github.com:LiqiLearningGroup/Git.git
git push -u origin master
```

## Clone LiqiLearningGroup repository into your own computer

edit by Prefocuson

First, get the repository address of LiqiLearningGroup

You can click into a specific repository to get its address on the right of "Clone or Download", get the address.
Like the image shown:
![Clone the repo address](/images/clone-the-repo-address.png)

Now you have copied the address of the repository(Git repo address is:git@github.com:LiqiLearningGroup/Git.git).Then open your command tool.

Choose a local folder to clone repository into. Use "cd" command to choose local folder.I get the folder named "Github"(the image below).

```Shell
git clone git@github.com:LiqiLearningGroup/Git.git
```

"Enter" to done it.

Now, you have succeed to clone the repository into your own folder.
![Clone folder](/images/clone-folder.png)

Then you can edit files by yourself. Using master or branch to edit, it's all ok, the way you like.

