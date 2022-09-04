1 create repo on GH
2 git remote add origin URL
3 git branch -M main (rename local master brancр to main)
4 git -u origin 'branchName' (main)
if first time on new gitHub repo => create access token (GH - Settings - Developer settings - Personal access token - Generate) or login to GH in opened window

# <!-- token saves in Windows Credentials manager  -->

git branch -a

<!-- shows local/localRemote and remote/origin branches -->

git branch -r

<!-- shows all emote/origin branches -->

git remote show origin

<!-- shows detailed configuration -->

git branch -vv

<!-- shows local tracking branches and their remotes  with more info -->

git ls-remote

<!-- shows all remote branches -->

gti fetch origin
updates all remotes/origin branches (create all remotes/origin witch is not in local but we have it on repo )

git pull
merging the remote changes into our local branches
works if we have local branches witch connected to remote
git pull origin doesn't works (need to specify branch name )

lacal br connected tj remote tracking br => git pull

git branch --track localBranchName origin/RemoteBranchName !!!!!!!!!

<!-- allows to track remote branch. now you can use git pull or push without typing ORIGIN -->

git branch --track origin/RemoteBranchName !!!!!!!!!

<!-- the same as prev but name will be as remote branch with "origin/branchName"-->

git push -u (-upstream) origin branch

<!-- will track remote  branch from start no need add --track command later  -->

===================================================
DE:LETE remote branch

1. delete local branch
2. git branch --delete --remotes branch <!--  delete remote tracking branch-->
3. git push origin --delete branchName <!--  delete remote tracking branch-->
   DELETE COMMIT LOCAL THEN REMOTE
4. git reset --hard (--soft) HEAD~1 <!-- delete local commit -->
git push origin branchName <!-- warning shown than we are behaind od origin branch we need force push-->
2. git push -F (--force) origin branchName <!-- we have updated remote branch -->

git clone URL

<!-- clone remote repo -->
