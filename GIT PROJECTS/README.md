# Initializing a Repository and Making Commits

## Initializing a Git Repository

First Download and Install git in your computer

Now to Initialize a git repo follow these steps:

 - Open a terminal on your computer, e.g git bash

 - On your terminal create your working folder or directory eg DevOps using this command `mkdir DevOps`

 - Change or move into your working directory or folder using this command `cd DevOps`

 - While you are inside the folder, run `git init` command

 ![Alt text](<Images/git 1.png>)

 ## Making your first Commit

 - Inside your working directory create a file index.txt using the command `touch index.txt`

 - Write any sentence you want using "echo". save your changes

 - Add your changes to git staging area using `git add .` Command

 - To commit your changes to git, run the command `git commit -m "initial commit"`

 ![Alt text](<Images/git 2.png>)

 # Working with Branches

 ## Making your first git Branch

 To make a new branch run this command `git checkout -b my-new-branch`

![Alt text](<Images/git 3.png>)

## Listing your git Branches

To list your git Branches run `git branch`

![Alt text](<Images/git 4.png>)

## Changing to an Old Branch

To change to an existing branch use this command `git checkout master`

![Alt text](<Images/git 5.png>)

## Merging Branch into another Branch 

Run `git merge B`

![Alt text](<Images/git 6.png>)

## Creating a New Repository and pushing your local git Repository to your remote github Repository

![Alt text](<Images/git 7.png>)

Add a remote repository to the local repository using this command

`git remote add origin <link to your github repo>`

![Alt text](<Images/git 8.png>)

After commiting your changes in your local repo, you push the content to the remote repo using this command 
`git push origin <branch name>`

To make a copy of remote repository in your local machine, use this command

`git clone <link to your remote repository>`

![Alt text](<Images/git 9.png>)


