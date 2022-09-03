git branch -D feature

<!-- delete feature branch -->

git reflog - shows all commits and stashes in current branch. For last 30 days

<!-- git reflog
ee1526e (HEAD -> master)
HEAD@{0}: reset: moving to HEAD^
17051aa HEAD@{1}: commit: all 3
ee1526e (HEAD -> master) HEAD@{2}: reset: moving to HEAD -->

git reset -hard `commit Hash from reflog`

<!-- если нужно вернуть в текущую ветку всё из удалённой ветки то процедура та же

если нужно вооссоздать удалённую ветку и изменения то: -->

1. git reflog
2. git checkout `commit Hash`
3. make new branch : git checkout -b 'name'
   <!-- will be thous changes on new branch -->

MERGING:

<!-- https://git-scm.com/book/en/v2/Git-Tools-Advanced-Merging#_advanced_merging -->
<!-- https://git-scm.com/docs/merge-strategies -->

Fast-forward merge

   <!-- быть на нужной ветку в которую нужно влить фичу напривер в мастер
   git merge feature залить в мастер все коммиты с фича ветки. HEAD на мастер переместится на последний коммит фича ветки -->

git merge --squash feature

<!-- залить в мастер только изменения. коммит создан не будет. изменения я с ветки фичи будут в staging area master branch-->
<!-- Squash commit -- not updating HEAD -->
<!-- need to create separate commit in master. HEAD will be on this lsat commit-->

NON Fast-forward merge

git merge --no-ff feature

on feature branch
gti rebase master

<!-- затянуть в фичу ветку новый мастер и поставить коммиты в очередности как на мастере. те сначала все комиты мастера потои будут идти комиты фичи -->

CONFLICTS

git log --merge

<!-- will show info about files with conflicts  -->

git merge --abort feature

<!-- cancel merge  -->

git diff

<!-- shows diffs in console -->

git cherry-pick #commit_hash

<!-- make copy of 1 any commit from target branch to master branch
it makes a new commit in master branch -->

git tag 'tag_name' commit_hash

<!-- add light weight comment to commit -->
<!-- view in git log:
commit 5f2ea7563db0f0d88d4a8fa8a0e56376002fd3f6 (tag: init) -->

git tag

<!-- shows tag list -->

git show 'tag name'

<!-- will show commit info and all changes -->

git checkout 'tag name'

<!-- will checkout to this commit  -->

git tag -d 'tag name'

<!-- delete tag -->

git tag -a 'tag name'

<!-- add tag to last commit  -->

Annotated tag
git tag -a(or commit hash) 'tag name' -m 'commit text'
adds lot of info to tag (Author, Date, commit tex, etc)
