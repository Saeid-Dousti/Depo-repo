# Demo

salaam! :)

## subheader

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

3- git checkout master --> to switch between branches (go to master)

4- 