
# git-master

## 1. version control?
-control version
-version control system is software that helps you control (or manage) the different version.
-there is a lot of version control
- ex) git, subversion, mercurial
- centralized model/ distributed model 
 the main point of a version control system is 
 to help you maintain a detailed history of the project 
 as well as the ability to work on different versions of it. Having a detailed history of a project is important because it lets you see the progress of the project over time. If needed, you can also jump back to any point in the project to recover data or files.

## 2. daily use of version control 
-undo is kind of version control
-google docs -> revision history ->check status(revision) version = revision // restore this version can make you start with old version 
- google docs
But for all its ability, it's not as powerful as we'd like. What's it missing? A few that I can think of are:

the ability to label a change
the ability to give a detailed explanation of why a change was made
the ability to move between different versions of the same document
the ability to undo change A, make edit B, then get back change A without affecting edit B
- version contol toll , git , can do all of those things. and more

## git and version contrrol 
<terminology> 
-version control system(VCS) === source code manager(SCM)
  
-commit (현상태 캡쳐): Git thinks of its data like a set of snapshots of a mini filesystem
 Every time you commit (save the state of your project in Git), it basically takes a picture of what all your files look like at that moment and stores a reference to that snapshot. You can think of it as a save point in a game - it saves your project's files and any information about them.
Everything you do in Git is to help you make commits, so a commit is the fundamental unit in Git.

- repository/ repo
a directory which contains your project work, as well as a few files 
Repositories can exist either locally on your computer or as a remote copy on another computer. A repository is made up of commits.

- working directory
 the files that you see in your computer's file system.
 When you open your project files up on a code editor, you're working with files in the Working Directory.
 
 This is in contrast to the files that have been saved (in commits!) in the repository.
 
 When working with Git, the Working Directory is also different from the command line's concept of the current working directory which is the directory that your shell is "looking at" right now. (?)
 
 -checkout 
A checkout is when content in the repository has been copied to the Working Directory. (?)

- Staging Area / Staging Index / Index
A file in the Git directory that stores information about what will go into your next commit. You can think of the staging area as a prep table where Git will take the next commit. Files on the Staging Index are poised to be added to the repository.

- SHA
A SHA is basically an ID number for each commit
It is a 40-character string composed of characters (0–9 and a–f) and calculated based on the contents of a file or directory structure in Git. "SHA" is shorthand for "Secure Hash Algorithm"

- branch
A branch is when a new line of development is created that diverges from the main line of development. This alternative line of development can continue without altering the main line.

you can think of a branch as where you make a save point in your game and then decide to try out a risky move in the game. If the risky move doesn't pan out, then you can just go back to the save point. The key thing that makes branches incredibly powerful is that you can make save points on one branch, and then switch to a different branch and make save points there, too.

working directory ->staging index -> commit -> repository


