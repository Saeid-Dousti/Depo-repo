# Demo

In this tutorial I have included the summary of the following tutorial video and git commands

[![GitHub issues](https://img.shields.io/github/issues/Saeid-Dousti/Git-tutorial-repo?style=plastic)](https://github.com/Saeid-Dousti/Git-tutorial-repo/issues)
[![GitHub forks](https://img.shields.io/github/forks/Saeid-Dousti/Git-tutorial-repo)](https://github.com/Saeid-Dousti/Git-tutorial-repo/network)
[![HitCount](http://hits.dwyl.com/Saeid-Dousti/https://githubcom/Saeid-Dousti/Git-tutorial-repo.svg)](http://hits.dwyl.com/Saeid-Dousti/https://githubcom/Saeid-Dousti/Git-tutorial-repo)

watch tutorial on youtube at 
https://www.youtube.com/watch?v=RGOj5yH7evk

### i) lets start

1- ls -la ---> to show you everything

2- git clone (ssh)

3- git add .  -> track files

4- git status

5- git commit -m "For the title of the update" -m "For the discription of the commit"

6- git restore --> restores to the latest commited version

7- ssh-keygen -t rsa -b 4096 -C "saeid1dousti@gmail.com"  -->  create the ssh key

8- cat id_rsa.pub

9- linking the ssh key to the local machine, 
    steps in https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

10- git push origin master
 or git push origin main
      
### ii) and now start a repo locally

1- git init --> to create repo on local machine rather than pulling it from github

2- git remote add origin git@github.com:Saeid-Dousti/Depo-repo2-from-local.git   -->  connects to a github repo    

3- git remote -v --> indicates the status of remote repo

4- git push origin master  -> to push to the repo
       -  git push -u origin master -> to set upstream at origin master so we don't have to right origin master each time we push

### iii) now branching

1- git branch ---> to know which branch we are at

2- git checkout -b feature-readme-instruction  --> to create a new branch

3- git checkout master --> to switch between branches (go to master) and shows the file in the new branch with updates and features!

4- git diff feature-readme-instruction     --->  showing the differences between the current branch and the one type in the command, i.e. feature-readme-instruction
    press q to end seeing the differences
    
5- git push -u origin feature-readme-instruction --> push the commited branch to a new branch on github

6- git merge 

### iv) After merging the branch to the main(master) branch

1- git branch -d feature-readme-instruction  ---> deleting the already merged branch

2- git commit -am "add and commit"  --> adds and commits ONLY a modified file not newly created file!

3- git merge --> this merge flags due to conflict
        Auto-merging index.html
        CONFLICT (content): Merge conflict in index.html
        Automatic merge failed; fix conflicts and then commit the result.
        
   on the index.html file we have 
        <<<<<<< HEAD
        <p>world</p>    
        =======
        <p>there</p>
        >>>>>>> main
    head is the branch we are at and after ==== line is the other branch

### v) Undoing at git

1- git reset README.md  --> this will reset (unstages) the added but not commited README.md

so I will add a line here and I add the README file but not commit it. 
 --- this line is not supposed to be here eeeeeeeeeeee---
 
2- git reset HEAD~1  ---> uncommits and unstages (removes what was added by add)

3- git log  ---> shows all the commits in reverse order
        resed what is added and commited

            commit fbdd4b966883845d99165add202b8558e250d424
            Author: Saeid Dousti <dousti_s@yahoo.com>
            Date:   Tue Nov 24 17:01:28 2020 -0500

fbdd4b966883845d99165add202b8558e250d424 is the commit hash

4- git reset fbdd4b966883845d99165add202b8558e250d424  --->  removes the commits after this commit but the lines related to those commits will be here only unstaged and uncommited

5- git reset --hard 200f14621f65e96485ac5a3cf44251363ef9e18a  --->  removes the commits after this commit + the lines related to those commits after this will be removed as well

6- git remote set-url origin new_url   --->   to reset the remote url that is renamed on github

### vi) Tagging at git

https://git-scm.com/book/en/v2/Git-Basics-Tagging  <---  git info website

Git has the ability to tag specific points in a repository’s history as being important. Typically, people use this functionality to mark release points (v1.0, v2.0 and so on). 
Git supports two types of tags: lightweight and annotated.

1- git tag  ---> lists all the existing tags

2- git tag -l "v1.8.5*"  --->  looks for tags with this pattern

3- git tag -a v1.4 -m "my version 1.4"  ---> creating annotated tags

4- git show v1.4  ---> That shows the tagger information, the date the commit was tagged, and the annotation message before showing the commit information.
tag v1.4
Tagger: Saeid Dousti <Dousti_s@yahoo.com>
Date:   Sat May 3 20:19:12 2014 -0700

my version 1.4

commit ca82a6dff817ec66f44342007202690a93763949
Author: Scott Chacon <schacon@gee-mail.com>
Date:   Mon Mar 17 21:52:11 2008 -0700

    Change version number

5-  git tag v1.4-lw  ---> creating lightweight tags
git show v1.4-1w
commit ca82a6dff817ec66f44342007202690a93763949
Author: Scott Chacon <schacon@gee-mail.com>
Date:   Mon Mar 17 21:52:11 2008 -0700

### vii) visual log

git can show the branches and commits in a graph:

1- gitk
    Change version number
