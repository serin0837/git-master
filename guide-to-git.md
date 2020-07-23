# code and stuff meet up

with jane
`git init`

git works by index

`git status`
`git add <>`
`git status`
`git commit` without file name
we go to squccle lien place
that mean give me file name
how can i get out of there?

git track changes
hello world-> welcome world
file changed, 1 insertion, 1 deletion

having chaged with local machine is good
but!
we go to second part which is remote
you dont have with local machine

create git repository

go to github

make new repository

copy the link of repo

git remote add origin paste url

git push origin master

ask user name and password

git repo added!!>\_<

### change something with repo

branch?
master
new branch?
`git checkout -b develop`
(-b: new branch)
:create new branch and go to that branch

> `git checkout --help` -- all of the documentation

make changes with that branch

ex) `git commit -am "redefined what this project is"`
_check what is this command_
`git commit -a`: add everything? ===`git add .`
`git push origin develop`

typical model? you have master branch
anything is live

develop: any working changes you have
add three things in your list

you going to put in develop

and then you merge with master

this branch is 1 commit ahead of master
-> insight -> network->
you can check
master < develop

missed merging part
pull request -> approved-> merge change together

make another change->
pull request ->

- merge pull request

master

o - o - o -o - o
\ /
o - o - o

conflict-> resolve confilct -> and merge back

`git checkout -b created-a`

add a file / changed READE.md

`git add .`
`git commit -m"Adde a.txt"`
`git push origin created-a`

- conflict?
  `git checkout develop` (go back to develop)
  `git checkout -b created-b`

add b file

git add .
git commit -m" added ~"

- network graph -> a bit painful

master -develop - creadted a
\ created b
created b -> develop b
create pull request ->
merge pull request
confirm merge

we merged them
so go back to develop
there is new file called b.txt

created a ->develop
create pull request
not let you thorugh because you have conlfict

see confilct
so need to make change

git pull origin develop( pull changes from github)
now can see b.txt

when you are merge?
`git merge created-a`

-> conflict
i am stil in develop
-> mix two thing together
(what is jane's name?)
J4Numbers/guide-to-git-demonstration
`git status`
git add .
git commit
:wp? (exit)

git push origin develop

but normally before merge
we need to check that can be stable

anyway we merge together

`git checkout <copy of sha>`
we are at that point of that commit
jump back to time

`git checkout -b created-c`
(we are in feature 3 and doing something)
add c.txt
change README.md

`git status`
`git add .`
`git commit -m"added c.txt"`
`git push origin created-c`

looking the network again

conflict
make change

git add .
git commit wP?

git push origin created-c

merge

working!horray!

pull / fetch?- fetch of all the detail -> can not see code in my local machine?

git pull -> apply the changes

then is it not better to keep doding with master?
and then co back to specific commit ?

- what if i don't want c?

`git -reflog?`
we want to reverse everthing that the point to made c

`git rebase -i` go something wrong?

git rebase -i 08 somthing

drop c file

:wp

and not there is merge conglict

rebase is going back time

and then in code editor change code

`git add .`
`git rebase --continue`

_then can i go to future?_

git push -u origin develop

rejected?
git push --force -u origin develop
(we are forcing our change)
make sure you not want to overwrite

- network looks clean

## reset

i want to go back to the point where it was working

reverse back to last poing

`git reset --hard HEAD`
head is go back last
and then reverted

you can also go back to specific point

`git reset --hard <sha>`
rewinding time

lost b.text as well

try to play around

tigkering

links

Guide to Git

resourese -> recommend to look

thank you so much contributing

i did not know how to go back to time
and merge and make another branch
wonder i can go to futere before you delete something?

think need to still practice..did not know there is so many command and sutff

merge : do not merge too big one

git-merge manual page

git- merge --help(all of documentation)
small

> guide-to-git-demonstration
> Guide-to-Git
