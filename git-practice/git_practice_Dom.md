# Git Pratice -1 
***
1. create new respository at local 
> git init  # will create a new .git hidden file at currently file.

2. copy a existing repository to local disk
> git clone <ssh://user@domain.com/repo.git>

3. changed file and add to buffer 
> vi filename # change file 
> git add <filename> # add filename to buffer
> or git add -a  # add all filename to buffer for submit

4. commit a change
> git commit -m "description"  # submit change(in buffer) file and submit it to the current file repo

5. upload current git repo to remote repo
> git push <remotea> <branch>

6. create a new branch
> git branch <new branch name>

7. list all existing branches
> git branch -av

8. switch HEAD branch
> git checkout <branch-nam>e

9. delete existing branch
> git branch -d <branch-name>
 
10. list all currently configured remotes
> git remote -v

11. git info. about which one remote
> git remote show <remote>

12. add new remote repo
> git remote add <shortname> <url>
> example: git remote add origin ssh:xxxxxx

13. update and merge currently repo.
> git pull <remote> <branch>

14. Publish local changes on a remote
> git push <remtoe> <branch>

15. Download all changes from <remote>, but dont intergrate into HEAD
> git fetch <remote>

16. Merge <branch> into your current HEAD
> git merge <branch>

17. Discard all lacal changes in your working directory
> git reset --hard HEAD

18. Discard local changes in specific file
> git checkout HEAD <ffile>

19. Rest a commit
> git revert --hard <commit>

20. Reset your HEAD pointer to a previous commit and discard all changes since then
> git reset --hard <commit>

