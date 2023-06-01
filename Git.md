# Git

Git is an open source Distributed version control system which allow us to work on different versions of the same file [i.e:like content tracker] or to work on the histories of a file. allow us to have backup.

different types of version control system,

1. Local VCS → in local file/server eg:filename_with_time_and_date
2. centralized VCS → have common server and allow users to have certain code and allow user to lock the code base which they are working, but here everyone don't have whole code eg: CVS, subversion, Preforce
3. Distributed VCS → everyone has a same updated version of code eg:Git locally and remote- GitHub, GitLab

Branch - Branch are nothing but pointers to a certain commit or to the previous commit.

Head → shows  where we are right now in the repository and points to the latest/last commit made in that branch. even if we switch the branch the head will also switch.

There are two types of merge 

1. fast-forward merge → which is the most common merge which git tries, when the current branch doesn’t have any commits after the new branch got created. if so it will perform fast forward merge.
2. no-fast-forward merge → here the current main branch/other will also have commits after the branch has been created. so now to merge it will create a new commit with merge message and then will merge two branches.

Commands

1. git init → to initialize the local repository
2. git config --global user.email "email" → to add the user email
3. git config --global user.name "name/id" → to add the user id
4. git config --global --list → to see the added username and email
5. git remote add origin <url> → to add the remote repository
6. git remote -v → to check the remote repo url
7. git remote remove origin → to remove the remote repo
8. git add <filename or . > → to add the files to the staging area
9. git status → to see the status of the file in stagin area or files history of commits
10. git commit -m "msg" → to commit the files in staging area
11. git push -u origin <main/branchname> → to push the commited changes to the remote repo
12. git branch -M main → to change the master branch as main branch
13. git push --all origin → to push all the branches
14. git pull <url> → to pull the remote repo to local or to pull specific remote branch to local and this will also update the local repo
15. git clone <url> → to have complete copy of the remote repo, mostly it will clone the main branch
16. git clone -b <branchname> <url> → to clone the exact branch we want and can also save it in name as we want
17. git fetch <url> → fetch all the latest changes to the repo but won't update it unlike pull
18. git pull origin main --allow-unrelated-histories → to overcome the non fast forward error
19. git log → to see all the previous commits and info about the commit hash, author and cmt date
20. git log --oneline → to see logs in less format and with less id characters (i.e: to view in compact way)
21. git log -n number → to see the last n number of commits
22. git show <commitd> → to see the changes we did in the particular commit
23. git branch → to see all the local branches
24. git branch <bname> → to create a branch
25. git branch -d <bname> → to delete the branch
26. git branch -a → to see both local and remote branches
27. git branch -C <branchname> → to create a new branch
28. git checkout -b <branchname> → to  create a new branch and switch to that branch 
29. git checkout/switch <branchname> → to switch between branches
30. git merge <bname> → to merge the given branch with the current branch
31. git merge <bname> -m "msg" → merge branch with cmt msg
32. git merge --no-ff <bname> → merge thebbranch without ff error
33. .gitignore → this file can be used for exception, if we don't want a file to be VC then use this file and mention those files inside this eg: like key, pswd
34. git checkout <filename> → to revert the file to previous version even if not made to staging area
35. git rm filename → to remove the file
    1. git rm - - cached <filename> → will just remove the file from git and tracking, the file will remain in the system (but not the best way to do because sometime we may accidentaly stage back again so use .gitignore)
    2. git rm -f <filename> → will also remove the file from the device
36. git diff → shows the changes we did before staging and now
37. git diff --cached → to revert back to prev version if the file is staged
38. git restore --staged <filename> → to remove it from the staging area (i.e: to unstage)
39. git revert cmtid → to get back to the cmt id but will leave a history
40. git revert HEAD → to get back to the previous commit
41. git reset --hard cmtid → revert back and don't leave any history and even del histories after the id
42. ssh-keygen.exe → to generate an ssh pub and priv key
43. ssh-keygen -t rsa -C email → will create an rsa based ssh pub and private key
44. git update -git-for-windows → to update the git

41. git rm --cached <filename> → to remove the file from cached so that it can be ignored by gitignore even though we commited it before

1. git restore <filename> → to discard the changes in the working directory. i.e: even before staging (note: this will be only for previously commited files)
    1. and it will also work in case where if we have a file that we staged and again we modified it, now it shows modified twice, one to be commited and other to be staged, here we can use git restore
2. git log - - name-only → to list the changed files as well
3. git reset --soft HEAD~1 → to revert the last change we made or commited
4. `git log --graph --decorate` → to see previous commit history along with the branch they were committed on
5. .
6. .
7. .
8. .
9. .

The URL that we used to connect the local and remote repository are called Connection string

origin is nothing but an aliasing name we give to an remote repository