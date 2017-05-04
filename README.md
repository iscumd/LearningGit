# LearningGit
Use this repo to learn Git. Fork, branch, commit, and submit a pull request!

## What is Git and GitHub?
Git is version control software. It allows you to track changes and collaborate when programming. GitHub is built on top of Git, using the standard software on your computer but adding extra features on the web.

The tutorials below may explain this better, but here is a quick summary of how Git works. 

You program like normal in a single folder (no copying different versions of files). When you set up Git, that folder becomes a "repository", or "repo". As you program, you will periodically take a snapshot of your repository and note your changes. This is called a "commit". 

When you want to add something, it is best to make a "branch" instead of committing directly to the "trunk", which is where we keep the mostly stable version of the project (sidenote: the trunk is actually just a special branch named "master"). This way, if something goes wrong or you want to work on something else, you can easily roll back your changes or switch to another version. After creating a branch and making your changes, you can merge those changes back into the trunk. [This tutorial](http://learngitbranching.js.org/) explains branching and merging in more detail.

Collaborating with others adds a couple extra steps. You will first need to "fork" the main repository by pressing the "Fork" button in the top right of a repository page on GitHub (there are other ways to fork, but this is the easiest). This makes a copy of the repository under your own account. Here you can make create a branch and make your changes. When you have finished your contribution, you will ask the main repository to merge in your branch by making a "pull request". You can do this by pressing the "New pull request" button on the main repository page.

## How do I get started?
1. Create a GitHub account. 
2. Download and install Git on your computer. I recommend using [GitHub Desktop](https://desktop.github.com/) on Windows and Mac instead of the standard command-line Git program because it does a lot of the annoying parts for you and provides a GUI that's more intuitive than the command-line interface. Linux users will need to use the standard command-line version of Git, which can be installed on most systems with `sudo apt-get install git`.
3. Download the GitHub repository to your computer. This is called "cloning" a repository. If you are using GitHub Desktop, you can select which of your own repositories you would like to clone by clicking the "+" button in the top left and then clicking "Clone". If you are using the command-line, copy the Git URL from the GitHub repository page by clicking the green "Clone or download" button and running `git clone <your .git URL here>` (example: `git clone https://github.com/iscumd/LearningGit.git`).

## Where can I find more information?
Here are some other good resources for learning Git.
* https://help.github.com/ - GitHub's knowledge base for almost every question you could have about Git and GitHub.
* https://try.github.io/ - A great interactive tutorial on the concepts used in Git. This also teaches the command-line commands.
* http://learngitbranching.js.org/ - A great interactive tutorial on branching and merging.
* https://www.git-scm.com/book/en/v2/Git-Basics-Undoing-Things - There will eventually come a time when you want to undo something. Forgot to commit a file? Accidentally staged a file? Want to undo changes to a file? This page explains how to do so from the command-line.

## TLDR: How to Actually use Git if you don't want Mr.PastaCello to yell at you
### SETUP
1. Fork desired ISC repo i.e https://github.com/iscumd/LearningGit.git
2. Git clone `git clone` your forked version of desired ISC repo i.e `git clone https://github.com/DrCurry/LearningGit.git`
3. navigate to the inside of the cloned directory i.e `cd https://github.com/iscumd/LearningGit.git`
4. Add the original ISC repo as an upstream i.e `git remote add upstream https://github.com/iscumd/LearningGit.git`
### EVERYTIME, Before you start working
5. To get the latest changes from the ISC repo `git pull upstream master`
6. Include overall ISC repo changes into your fork `git push origin`
### AFTER Working on your repo
7. 







