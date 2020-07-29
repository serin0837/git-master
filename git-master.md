## maniging timeline

Basic timeline requirements
Store content of file and directories
Add new "points" to the timeline
View the changes we've made since the last point in our time line
Move between between the points in the timeline

git is version control software and some of its most basic features will allow us to fulfill all the requirements of a basic content timeline.

# 1. version control?

-control version
-version control system is software that helps you control (or manage) the different version.
-there is a lot of version control

- ex) git, subversion, mercurial
- centralized model/ distributed model
  the main point of a version control system is
  to help you maintain a detailed history of the project
  as well as the ability to work on different versions of it. Having a detailed history of a project is important because it lets you see the progress of the project over time. If needed, you can also jump back to any point in the project to recover data or files.

## daily use of version control

-undo is kind of version control
-google docs -> revision history ->check status(revision) version = revision // restore this version can make you start with old version

- google docs
  But for all its ability, it's not as powerful as we'd like. What's it missing? A few that I can think of are:

the ability to label a change
the ability to give a detailed explanation of why a change was made
the ability to move between different versions of the same document
the ability to undo change A, make edit B, then get back change A without affecting edit B

- version contol toll , git , can do all of those things. and more

## git and version control

<terminology> 
-version control system(VCS) === source code manager(SCM)
  
-commit (현상태 캡쳐): Git thinks of its data like a set of snapshots of a mini filesystem
 Every time you commit (save the state of your project in Git), it basically takes a picture of what all your files look like at that moment and stores a reference to that snapshot. You can think of it as a save point in a game - it saves your project's files and any information about them.
Everything you do in Git is to help you make commits, so a commit is the fundamental unit in Git.

- repository/ repo
  a directory which contains your project work, as well as a few files
  Repositories can exist either locally on your computer or as a remote copy on another computer. A repository is made up of commits.

- working directory
  👩The working directory refers to all of the files and directories we can currently view and edit in our project.

  the files that you see in your computer's file system.
  When you open your project files up on a code editor, you're working with files in the Working Directory.

This is in contrast to the files that have been saved (in commits!) in the repository.

When working with Git, the Working Directory is also different from the command line's concept of the current working directory which is the directory that your shell is "looking at" right now. (?)

-checkout
A checkout is when content in the repository has been copied to the Working Directory. (?)

- Staging Area / Staging Index / Index
  A file in the Git directory that stores information about what will go into your next commit. You can think of the staging area as a prep table where Git will take the next commit. Files on the Staging Index are poised to be added to the repository.

- SHA [샤]
  A SHA is basically an ID number for each commit
  It is a 40-character string composed of characters (0–9 and a–f) and calculated based on the contents of a file or directory structure in Git. "SHA" is shorthand for "Secure Hash Algorithm"

- branch
  A branch is when a new line of development is created that diverges from the main line of development. This alternative line of development can continue without altering the main line.

you can think of a branch as where you make a save point in your game and then decide to try out a risky move in the game. If the risky move doesn't pan out, then you can just go back to the save point. The key thing that makes branches incredibly powerful is that you can make save points on one branch, and then switch to a different branch and make save points there, too.

working directory ->staging index -> commit -> repository

## Git config

### git config --list(show me the configure list )

# 2. create a git repo

## git init

.git is repository
hidden directory
`rm -rf .git`
what is inside .git?
config file, hooks directory...

## clone and existing repo

git clone <url>
Verify Terminal Location

TIP: Now before you clone anything, make sure you are located in the correct directory on the command line. Cloning a project creates a new directory and places the cloned Git repository in it. The problem is that you can't have nested Git repositories. So make sure the terminal's current working directory isn't located in a Git repository. If your current working directory is not in your shell's prompt, type pwd to print the working directory.
(👩what is this means?)

Cloning into 'course-git-blog-project'...". Git is creating a directory (with the same name of the project we're cloning) and putting the repository in it

The rest of the output is basically validation - it's counting the remote repository's number of objects, then it compresses and receives them, then it unpacks them.

### clone with different name?

add another name after same command

Not In A Git Repository?
WARNING: Here's a very important step that often gets missed when you first start working with Git. When the git clone command is used to clone a repository, it creates a new directory for the repository...you already know this. But, it doesn't change your shell's working directory. It created the new repo inside the current working directory, which means that the current working directory is still outside of this new Git repo! Make sure you cd into the new repository.

Remember to use the Terminal's command prompt as an aid - if you're in a directory that is a Git repository, the command prompt will include a name in parentheses.

## Determine a repo's status

The output tells us two things:

On branch master – this tells us that Git is on the master branch. You've got a description of a branch on your terms sheet so this is the "master" branch (which is the default branch). We'll be looking more at branches in lesson 5
Your branch is up-to-date with 'origin/master'. – Because git clone was used to copy this repository from another computer, this is telling us if our project is in sync with the one we copied from. We won't be dealing with the project on the other computer, so this line can be ignored.
nothing to commit, working directory clean – this is saying that there are no pending changes.

This command will:

tell us about new files that have been created in the Working Directory that Git hasn't started tracking, yet
files that Git is tracking that have been modified
a whole bunch of other things that we'll be learning about throughout the rest of the course ;-)

---

# Create A GIt Repo

1. `mkdir -p udacity-git-course/new-git-project && cd $_`
   I made file path and cd to there
2. git init

## command

git init
create a new git repository

ls -a
we can print all the files and directories including those directories that start with a .

git will register that the working directory has been updated and we can view this information by running the git status command
(An untracked file is a newly created file that has not yet been stored inside the git repository.)

The staging area is an area inside git where we store all the changes that we want stored in our next snapshot.

We can use the git add command in order to stage these changes.

Working directory:
Staging area:
Git repository:

It is our goal ultimately to store a snapshot of our file and directories so we can start to create a timeline consisting of snapshots of our project.
git commit -m <commit-message-here>.

first commit is root commit

git log
We can use the command git log to list all the commits stored inside a git repository. You can also think of git log as printing the timeline of different commits in our project.

# Branches and Github

## master branch

(👩default new empty git repository)
A branch in git is often referred to as a series of commits that forms a timeline representing some work in a project.

However, we need only point a single commit as this one points back the others.

The branch that is created by default when a new empty git repository is created is the master branch.
Whenever a new git commit is created then master branch is updatd so it points to the most recent commit.

## Github?

Github is a website that stores github repositories in the cloud and allows multiple users to store their work so that each collaborator can share their changes online.

## remote

A remote repository is one stored on github

- a new github repository will be referred to as origin.

## git remote add origin <origin-repository-url>

When a new repository is created on github then a new url is generated which points to the remote repository on github. We can use this url to connect a local machine with a github repo so work can be retrieved from the remote and so the remote can be updated with any local commits.
Once this command has been executed this can be checked by running
(👩그냥 바로 클론 하면 안되나요?)

## git remote -v

## git push

git push will add the three local commits on to the master branch of the origin repository.
We can use the git push command in the following way:
git push origin master

Once this command is executed both the local master branch and the origin master branch abbreviated as origin/master will be pointing at the same commit. In this commit, both the local and the remote master branches are up to-date.

## example of command connecting to different repository

1. git remote -v (check now)
2. git remote remove origin
3. git remote -v (double check that it's removed, see nothing)
4. git remote add origin <URL>
5. git remote -v
6. git push origin master

# 3. Review repo history

## intro

- git log
- git show : displays information about the given commit

## displaying a repository's commit

- git log ->

1. to scroll down, press

- j or ↓ to move down one line at a time
- d to move by half the page screen
- f to move by a whole page screen

2. to scroll up, press

- k or ↑ to move _up_ one line at a time
- u to move by half the page screen
- b to move by a whole page screen

  can keep see all the log

  > if want to be out of log press `Q`

## changing how git log displays info

`git log --oneline`
one line changed how it displays
:6 first sha and commit message

## viewing modified files

`git log --stat`(stat:statistics)

- displays the files that have been changed
- display the numbers of lines that have been added/removed
- displays a summary line

## viewing file changes

`git log -p`(--patch)

- displays the files that have been modified
- displays the location of the lines that have been added/removed
- displays the actual changes that have been made

diff === patch
show original version and changed version
show different changes in same file
index hash original ver / hash changed ver <- not really useful
@@ start line, original how many line/ start line, how many changed line
bottom is actual code that changed
-: removed
+: added

`git log -p --stat` show both
`git log --stat -p` show both

`git log -p -w` will show the patch information, but will not highlight lines where only whitespace changes have occurred.

## viewing a specific commit

example :`git log -p fdf5493`
provide specific SHA
`git show`
most recent commit

displayed exactly same info with `git log -p` command

`git show` can be combied with most of other flags
