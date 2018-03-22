# LearningGit
Use this repo to learn Git. Fork, branch, commit, and submit a pull request!

## What is Git and GitHub?
Git is version control software. It allows you to track changes and collaborate when programming. GitHub is built on top of Git, using the standard software on your computer but adding extra features on the web.

The tutorials below may explain this better, but here is a quick summary of how Git works. 

You program like normal in a single folder (no copying different versions of files). When you set up Git, that folder becomes a "repository", or "repo". As you program, you will periodically take a snapshot of your repository and note your changes. This is called a "commit". 

When you want to add something, it is best to make a "branch" instead of committing directly to the "trunk", which is where we keep the mostly stable version of the project (sidenote: the trunk is actually just a special branch named "master"). This way, if something goes wrong or you want to work on something else, you can easily roll back your changes or switch to another version. After creating a branch and making your changes, you can merge those changes back into the trunk. [This tutorial](http://learngitbranching.js.org/) explains branching and merging in more detail.

Collaborating with others adds a couple extra steps. You will first need to "fork" the main repository by pressing the "Fork" button in the top right of a repository page on GitHub (there are other ways to fork, but this is the easiest). This makes a copy of the repository under your own account. Here you can create a branch and make your changes. When you have finished your contribution, you will ask the main repository to merge in your branch by making a "pull request". You can do this by pressing the "New pull request" button on the main repository page. In order to update your local repository if others have made changes to the main ISC repository (i.e. done the above steps), you will need to:
1. `git checkout master`
2. `git pull upstream master` and resolve any merge conflicts

For ISC ROS work, it is suggested to clone repositories into the `catkin_ws/src` folder, i.e. `catkin_ws/src/RepositoryName/*` where the `*` would contain `src`, `msg`, etc. 

## How do I get started?
1. Create a GitHub account. 
2. Download and install Git on your computer. I recommend using [GitHub Desktop](https://desktop.github.com/) on Windows and Mac instead of the standard command-line Git program because it does a lot of the annoying parts for you and provides a GUI that's more intuitive than the command-line interface. Linux users will need to use the standard command-line version of Git, which can be installed on most systems with `sudo apt-get install git`.
3. Download the GitHub repository to your computer. This is called "cloning" a repository. If you are using GitHub Desktop, you can select which of your own repositories you would like to clone by clicking the "+" button in the top left and then clicking "Clone". If you are using the command-line, copy the Git URL from the GitHub repository page by clicking the green "Clone or download" button and running `git clone <your .git URL here>` (example: `git clone https://github.com/iscumd/LearningGit.git`).

## Step-by-Step
### Setup
1. Fork the desired repository by clicking the **Fork** button in the top right of the GitHub page.  
![Fork button](http://i.imgur.com/BMPjjhK.png)
2. Go to where you want to work on the repository, open a terminal there, and **clone** your forked repository with `git clone https://github.com/YOUR_USERNAME/LearningGit.git`. You can copy that URL from your repository's GitHub page.  
![Clone button](http://i.imgur.com/uvuHkC9.png)
3. Navigate to the inside of the cloned directory with `cd LearningGit`.
4. Add the original repository as a **remote** named `upstream` with `git remote add upstream https://github.com/iscumd/LearningGit.git`.
5. Set the **user email** for the repo to the same email as your GitHub account with `git config user.email "you@example.com"`. If the computer you are working on is your personal machine, use `git config --global user.email "you@example.com"`. **DO NOT** use the `--global` flag if you are on a shared machine such as a club laptop.
### Everytime before you start working
1. Switch to the `master` branch with `git checkout master`.
2. Update your local repository with the changes in the `upstream` repository with `git pull upstream master`.
3. When you start a new set of related changes, you make a **branch** with `git checkout -b branch_name`. Change `branch_name` to a meaningful name related to what your new changes will be.
### Periodically while you are working
1. **Add** your files that need to be submitted with `git add README.md`. You may also add more than one file at once with `git add file.txt README.md pic.jpg`. Make sure there are spaces between files, and you can use Tab to quickly complete filenames. Use `git status` to see the files that are staged, files that are changed but not staged, and other useful information.
2. **Commit** your changes with `git commit -m "Commit message"`. The -m is the flag for adding a commit message, and it should contain helpful information on the changes you made in that commit such as `git commit -m "Start joystick node"` (by convention, commits that start with a verb have the verb in the imperative mood, like if you were commanding someone to *start*).
### When you are done working
1. Make sure all your changes are commited with `git status`.
2. **Push** your changes to your repository on GitHub with `git push -u origin branch_name` and supply your GitHub login credentials. The `-u` flag associates your local branch with the remote branch.
3. Go to [github.com](github.com) and login. Go to your repository (`https://github.com/YOUR_USERNAME/LearningGit`) then click on **Compare & pull request**.  
![Compare & pull request button](http://i.imgur.com/BN2K8h4.png)

## Where can I find more information?
Here are some other good resources for learning Git.
* https://help.github.com/ - GitHub's knowledge base for almost every question you could have about Git and GitHub.
  * [Configuring a Remote for a Fork](https://help.github.com/articles/configuring-a-remote-for-a-fork/)
  * [Syncing a fork](https://help.github.com/articles/syncing-a-fork/)
* https://try.github.io/ - A great interactive tutorial on the concepts used in Git. This also teaches the command-line commands.
* http://learngitbranching.js.org/ - A great interactive tutorial on branching and merging.
* https://www.git-scm.com/book/en/v2/Git-Basics-Undoing-Things - There will eventually come a time when you want to undo something. Forgot to commit a file? Accidentally staged a file? Want to undo changes to a file? This page explains how to do so from the command-line.

