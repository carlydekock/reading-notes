# Revisions and the Cloud

#### Terms and Definitions
- **Version Control**: system that allows you to revisit various versions of a file (or set of files) by recording changes
- **Local**: On your own computer, on your personal hard disk where files and changes are stored
- **Centralized Version Control System (CVCS)**: single server storing all changes and file versions, can be accessed by various people. CVS can present an issue in that it is a single point of failure, risks work being lost.
- **Distributed Version Control System (DVCS)**: this allows you to create mirrored repositories, allows teams to work together and collaborate
- **Git**: A DVCS that stores data in a file system made up of snapshots or changes made. Git mostly relies on local operations, allows for process expediency, and allowing for work on a project even when not online or on a VPN. 
- **Commit**: When you save a changed version of your project
- **States**: Files in Git can reside in three main states:
  - Committed: data is securely stored in a local database
  - Modified: file has been change but not yet committed
  - Staged: Flagged a file's changed version, yet to be committed

## History of Git
Founded in 2005 by Linus Torvalds, the chief architect of the Linux kernel. 
One of the most utilized VCS in the world.
Special because it allows for non-linear development via  multiple branches, support of large projects, strong capability for preventing corruption of files, and simple design.

## Getting Git setup
1. Download Git: either install as a package, install via another installer, or download and compile the source code.
1. Customize Git (one time setup): 
   1. Identity setting: Setting the username and password
      1. Use the `git config` command to set user.name and user.email (the name and email associated with your GitHub account)
   1. Configure your desired text editor, or Git will use the system's default editor
   1. To check settings, use the `git config --list` command
   1. For help, here are three ways to get more info on a particular command:
      1. `git help command`
      1. `git command --help`
      1. `man git-command`
1. Setting up a Git Repository (from terminal): 
   1. Switch to the target directory using the cd command
   1. Use the `git init` command to create a new repository
   1. To start tracking, perform an initial commit by typing:
      1. `git add *.c`
      1. `git add LICENSE`
      1. `git commit -m "insert comment text here"`
1. Cloning a file: using the command `git clone https://...` with the URL of the page you want to clone
   1. To clone a repository into directory with another name, use `git clone https://... mydirectory` with the URL of the page you want to clone and the name of your new directory
1. Check state of files using `git status` command

## Workflow of Git
Local Git repository has three components:
1. Working directory: the actual files reside here
1. Index: the area used for staging
1. Head: Points to the most recent commit

All files are either **tracked** (can be modified, unmodified or staged; part of the most recent file snapshot) or **untracked** (not in the last snapshot; currently not in the staging area)

## Life Cycle of Files
1. After you edit a file, Git flags it as modified
1. You stage the modified file
1. Then, you commit the staged changes

## **ACP Process**: Add, commit, push
1. Add: Track one file using the following: `git add filename` or multiple files using `git add .`
1. Commit: After staging your files, commit the changes and record what you did with a message: `git commit -m "insert message of what you did"`
1. Push: This is to push the changes to your remote repository: `git push origin main`

## Other info:
- `git stash` stashes any changes you are not ready to commit, but don't want to lose
- `git stash apply` retrieves the hidden changes


[<==Back](code102contents.md)
