# Git & GitHub Fundamentals Lab

## Project Overview

This project demonstrates my understanding of Git and GitHub workflows.
It includes practical examples of commits, branches, merges, and pull requests.

## What I Learned

- How to initialize a Git repository
- How to stage and commit changes
- How to create and switch branches
- How to merge branches
- How pull requests work on GitHub

## Git Commands Practiced

- git init
- git add
- git commit
- git branch
- git switch
- git merge
- git push

## Why This Matters for DevOps

Version control is essential in DevOps and cloud engineering.
Infrastructure-as-Code tools like Terraform rely heavily on Git workflows.
Understanding branching and pull requests is critical for CI/CD pipelines.

# Learning Git


## Initialising and configuring Git
#### I already had Git installed on my Mac, I used the version command to find the exact version that I have installed
```
git --version
```
![git init](images/git_init.png)

#### Next I had to configure my global username and user email, I did this with the git config command
```
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```
![config](images/git_config.png)

#### To verify that this was done correctly I used the list command.
```
git config --list
```
![list](images/git_config_list.png)

## Creating my first project
#### To do this I have to use the make directory command "mkdir" and then I had to use the change directory command "cd" to switch to the correct directory
```
mkdir git-lab
cd git-lab
```
![mkdir](images/mkdir.png)

#### Now that I had created and moved to my new directory called "git-lab", I had to use the "init" command to initialise the directory
```
git init
```
![init 2](images/init_git_2.png)

## Creating a file
#### Now that I had my git directory created and initialised it was time to create my first file, I did this using the "touch" command, I then used the "nano" command to edit the file
```
touch README.md
nano README.md
```
![read me](images/git_readme.png)
![edit read me](images/edit_readme.png)


## My first commit
#### Now that I had created my first file I was ready to commit it, the first step was to check it's status
```
git status
```
![status](images/git_status.png)

#### Then I had to stage the file using "git add"
```
git add README.md
```
![stage](images/git_stage.png) 

#### Finally I had to commit the file, when committing changes it is best pratice to add a message, with git you can do this with "-m".
```
git commit -m "Initial commit - added README"
```
![commit](images/git_commit.png)

## Understanding Branches
#### During development, teams will use different branches to work on update, this is done to test changes before committing them directly to the main branch, I wanted to practice this concept, I did this by creating a new branch called "feature-update", I then had to switch to the new branch using the "switch" command

```
git branch feature-update
git switch feature-update
```
![branches](images/branches.png)

#### Now that I was working from the new branch I decided to edit the read me file I had created

![edit](images/nano_branch.png)

#### Once my edits had been made I committed them with a message to follow best practices
```
git add README.md
git commit -m "Added feature branch section"
```
![branch commit](images/branch_commit.png)

#### I then had to merge the two branches together, to do this I switched back to the main branch and used the "merge" feature to merge the two branches together
```
git switch main
git merge feature-update
```
![switch main](images/switch_main.png)
![merge b](images/merge_branch.png)

## Pushing to GitHub
#### To push my work to my GitHub account I had to make a new repository, I called this one "git-fundamentals-lab". I then had to connect my local repository to my GitHub with the following commands.

```
git remote add origin https://github.com/yourusername/git-fundamentals-lab.git
git branch -M main
git push -u origin main
```
![git connect](images/git_connect.png)
![GH](images/GH.png)

## Creating a Pull Request
#### first I wanted to create a new branch and switch to it simultaneously

```
git switch -c improve-readme
```
![imp read](images/imp_read.png)

##### I then edited my Read me file and then committed the changes as I did before, I then pushed the branch with the following command

```
git push origin improve-readme
```
![git push](images/git_push.png)

#### On my GitHub account I then saw "Compare & Pull Request", I then created a pull request and merged the changes to the main branch.



