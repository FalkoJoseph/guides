Git worflow
-----------

0. Shortcuts
============

$g st (status)
$g aa (add all)
$g push
$g up (rebase)
$g co (checkout)


1. Getting the latest changes
=============================

$git fetch

$git rebase origin/master

(if succesfull):

  $git push origin <branch> -f

(if not succesfull):

  solve problems in files

  $git rebase --continue

  $git push origin <branch>

2. Merging with master branch
=============================

Merge via github.com

Delete branch

3. Delete old branch locally
============================

$git checkout master

$git branch -D <old_branch>
$git push origin :<old_branch>

4. Get the latest changes from master
=====================================

$git pull

5. Create a new branch
======================

$git checkout -b <new_branch>

$git push origin <new_branch>

5. Remove cached files (updated gitignore)
==========================================

$git rm -r --cached .

$git add .

$git commit -m ".gitignore is now working"

6. Reset current branch
=======================

$git reset --hard origin/master
