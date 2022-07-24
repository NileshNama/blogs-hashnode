## Getting started with Git & GitHub

# Git vs Github
**Git**  is a version control system that lets you manage and keep track of your source code history. **GitHub** is a cloud-based hosting service that lets you manage Git repositories. If you have open-source projects that use Git, then GitHub is designed to help you better manage them. 

![Git VS Github.jpg](https://github.com/NileshNama/NileshNama/blob/main/Git%20VS%20Github.jpg align="left")

---

# Some Git CLI commands

## Git : Configure

    git config --global user.email "youremail@example.com " sets email address respectively to be used with your commits.
    
    git config --global user.name "FirstName LastName" sets the author name.
    
    git config --list command to list all the settings Git can find at that point.
    
    git config --global color.ui true Git automatically colors of its output.

## Git : commit to repository

    git commit -m "Add three files" command records or snapshots the file permanently in the version history.
    
    git commit --amend -m <enter your message> command allows you to change the commit message.

## Git : branching

    git branch command lists all the local branches in the current repository.
    
    git branch <branch-name> command creates a new branch.
    
    git checkout <branch-name> command is used to switch from one branch to another.
    
    git merge <branch-name> command merges the specified branch’s history into the current branch.
    
    git checkout -b <branch-name> command creates a new branch and also switches to it.

## Git : Initiating a repository

    git init command is used to start a new repository.
    
    git status command lists all the files that have to be committed.

## Git : Pulling & pushing from and to repositories

    git remote add origin <link-to-repo> ommand is used to connect your local repository to the remote server.
    
    git push -u origin main command sends the committed changes of main branch to your remote repository.
    
    git clone <link-to-clone-repo> command is used to obtain a repository from an existing URL.
    
    git pull command fetches and merges changes on the remote server to your working directory.

## Git : Staging

    git add <file-name> command adds a file to the staging area.
    
    git add <file-name> <second-file-name> <third-file-name> command adds one or more files to the staging area.
    
    git add . command adds all files under the current directory to the staging area.
    
    git add --all command finds all new and updated files everywhere throughout the project and add them to the staging area.
    
    git add -A Same as --all
    
    git rm --cached <file-name>

---