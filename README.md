https://www.bogotobogo.com/cplusplus/Git/Git_GitHub_Source_Tree_3_Git_WorkFlow.php

If you want to list all the files currently being tracked under the branch master, you could use this command:
git ls-tree -r master --name-only

If you want a list of files that ever existed (i.e. including deleted files):
git log --pretty=format: --name-only --diff-filter=A | sort - | sed '/^$/d'










GIT EDITOR to VI
----------------

git config -l

git config --global core.editor "vi"

GIT_EDITOR=vi

export GIT_EDITOR



GIT
----
root@raspberrypi:~/# git clone  https://github.com/amitsuneja/robotic_car.git

root@raspberrypi:~/# ssh-keygen and copy key to GIT

root@raspberrypi:~/# cd robotic_car

root@raspberrypi:~/robotic_car# git remote set-url origin ssh://git@github.com/amitsuneja/robotic_car.git

root@raspberrypi:~/robotic_car# git push

Everything up-to-date

root@raspberrypi:~/robotic_car#



# Learning Git (Distributed Version Control)
# Keeping History of working versions of project
# Know who make changes and why and when 
# Merge conflicting changes
# https://git-scm.com/



sun01$ echo "# learninggit" >> README.md


sun01$ git init



sun01$ git add README.md




sun01$ git commit -m "first commit"



sun01$ git remote add origin https://github.com/amitsuneja/learninggit.git



sun01$ git push -u origin master

Username for 'https://github.com': amitsuneja

Password for 'https://amitsuneja@github.com':






sun01$ git clone https://github.com/amitsuneja/learninggit.git

sun01$ cd learninggit

sun01$ mkdir dir1

sun01$ touch dir1/file1


sun01$ git add dir1

sun01$ git add dir1/file1



sun01$ git commit -am "My 6th commit"



sun01$git push

Username for 'https://github.com': amitsuneja

Password for 'https://amitsuneja@github.com':



















# Making Git Passwordless

Login to EC2
use ssh-keygen
cat ~/.ssh/id_rsa.pub

login to GitHub > Profile > SSH and GPG Keys > New ssh Key > GiveTitel and SaveKey 

sun01$ git remote show origin
* remote origin
  Fetch URL: https://github.com/amitsuneja/learninggit

  Push  URL: https://github.com/amitsuneja/learninggit



sun01$ git remote set-url origin git+ssh://git@github.com/amitsuneja/learninggit


sun01$ git remote show origin
* remote origin
  Fetch URL: git+ssh://git@github.com/amitsuneja/learninggit


  Push  URL: git+ssh://git@github.com/amitsuneja/learninggit




# Adding .gitignore file in  project directory
sun01$ cat .gitignore

*.swp




# Git Fundamentals
# git diff - compare working directory with staging area

WorkingDirectory -------git add--------------> StagingArea -------git commit------------->Respository(CommitedFiles)
#




sun01$ git diff


diff --git a/README.md b/README.md
index 316b8b7..a11ea64 100644
--- a/README.md
+++ b/README.md
@@ -114,3 +114,10 @@ sun01$ cat .gitignore

 *.swp

+
+
+
+# Git Fundamentals
+
+
+WorkingDirectory -------git add--------------> StagingArea -------git commit------------->Respository(CommitedFiles)




sun01$ git add .


sun01$ git diff











# git checkout
use git log then below commands

[linux01]# git checkout 9ec1078b068a1e746ab537ec2e54acfaae7275dd


HEAD is now at 9ec1078... second



[linux01]# cat Readme.md

Test

hello how are you




[linux01]# git checkout 53310769efaf341734c4b609bdf29d9449736271

Previous HEAD position was 9ec1078... second

HEAD is now at 5331076... first



[linux01]# cat Readme.md


Test


[linux01]#




# Branches

[linux01]# git branch BranchForDeveloper2

[linux01]# git push origin BranchForDeveloper2

Total 0 (delta 0), reused 0 (delta 0)

To git+ssh://github.com/amitsuneja/troposphere

 * [new branch]      BranchForDeveloper2 -> BranchForDeveloper2


[linux01]#

Now on git hub do below
settings of your Project > collaborators > search name example sarastanway@gmail.com or type sara and Add > it will be awating for sara response.






