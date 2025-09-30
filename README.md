# Gitexercises-2
# part one codes

```bash

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises
$ cd 'c:/Users/user/Desktop/githubexercises/Gitexercises-2'

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (main)
$ git checkout dev
error: pathspec 'dev' did not match any file(s) known to git

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (main)
$ git checkout -b dev
Switched to a new branch 'dev'

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ touch test{1..4}.md

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git add test2.md

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git commit -m "chore: Create initial file"
[dev 248f285] chore: Create initial file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test2.md

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$
git add test2.md

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git commit -m "chore: Create another file"
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        test1.md
        test3.md
        test4.md

nothing added to commit but untracked files present (use "git add" to track)

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git add test3.md

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git commit -m "chore: Create third and fourth files"
[dev 8d36353] chore: Create third and fourth files
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git add test4.md

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git commit --amend -m "chore: Create third and fourth files including missing test4.md"
[dev 77cbad3] chore: Create third and fourth files including missing test4.md
 Date: Tue Sep 30 13:42:07 2025 +0200
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md
 create mode 100644 test4.md

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git rebase -i HEAD~2
hint: Waiting for your editor to close the file... unix2dos: converting file C:/Users/user/Desktop/githubexercises/Gitexercises-2/.git/rebase-merge/git-rebase-todo to DOS format...
dos2unix: converting file C:/Users/user/Desktop/githubexercises/Gitexercises-2/.git/rebase-merge/git-rebase-todo to Unix format...
hint: Waiting for your editor to close the file... unix2dos: converting file C:/Users/user/Desktop/githubexercises/Gitexercises-2/.git/COMMIT_EDITMSG to DOS format...
dos2unix: converting file C:/Users/user/Desktop/githubexercises/Gitexercises-2/.git/COMMIT_EDITMSG to Unix format...
[detached HEAD 09200d9] chore: Create third and fourth files (added missing test4.md)
 Date: Tue Sep 30 13:42:07 2025 +0200
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md
 create mode 100644 test4.md
Successfully rebased and updated refs/heads/dev.

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git log --oneline
09200d9 (HEAD -> dev) chore: Create third and fourth files (added missing t
est4.md)
248f285 chore: Create initial file
8e6fe2d (origin/main, origin/HEAD, main) Initial commit

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ echo "temporary file" > unwanted.txt

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git add unwanted.txt
warning: in the working copy of 'unwanted.txt', LF will be replaced by CRLF the next time Git touches it

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git commit -m "Unwanted commit"
[dev e077ea5] Unwanted commit
 1 file changed, 1 insertion(+)
 create mode 100644 unwanted.txt

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git rebase -i HEAD~N
fatal: invalid upstream 'HEAD~N'

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git log --oneline
e077ea5 (HEAD -> dev) Unwanted commit
09200d9 chore: Create third and fourth files (added missing test4.md)
248f285 chore: Create initial file
8e6fe2d (origin/main, origin/HEAD, main) Initial commit

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git rebase -i HEAD~2
hint: Waiting for your editor to close the file... unix2dos: converting file C:/Users/user/Desktop/githubexercises/Gitexercises-2/.git/rebase-merge/git-rebase-todo to DOS format...
dos2unix: converting file C:/Users/user/Desktop/githubexercises/Gitexercises-2/.git/rebase-merge/git-rebase-todo to Unix format...
Successfully rebased and updated refs/heads/dev.

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git log --oneline
09200d9 (HEAD -> dev) chore: Create third and fourth files (added missing test4.md)
248f285 chore: Create initial file
8e6fe2d (origin/main, origin/HEAD, main) Initial commit

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git rebase -i HEAD~2
hint: Waiting for your editor to close the file... unix2dos: converting file C:/Users/user/Desktop/githubexercises/Gitexercises-2/.git/rebase-merge/git-rebase-todo to DOS format...
dos2unix: converting file C:/Users/user/Desktop/githubexercises/Gitexercises-2/.git/rebase-merge/git-rebase-todo to Unix format...
error: could not parse 'abc123'
error: invalid line 2: pick abc123 chore: Create initial file
You can fix this with 'git rebase --edit-todo' and then run 'git rebase --continue'.
Or you can abort the rebase with 'git rebase --abort'.

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev|REBASE)
$ git log --oneline --graph
REBASE)
$ git checkout -b ft/branch
Switched to a new branch 'ft/branch'

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev|REBASE)
$ echo "This is test5 file" > test5.md

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev|REBASE)
$ git rebase --continue
error: could not parse 'abc123'
error: invalid line 2: pick abc123 chore: Create initial file
error: please fix this using 'git rebase --edit-todo'.

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev|REBASE)
$ git rebase --abort

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git checkout -b ft/branch
fatal: a branch named 'ft/branch' already exists

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git checkout  ft/branch
Switched to branch 'ft/branch'

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (ft/branch)
$ git status
On branch ft/branch
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        test1.md
        test5.md

nothing added to commit but untracked files present (use "git add" to track)

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (ft/branch)
$ git add test5.md
warning: in the working copy of 'test5.md', LF will be replaced by CRLF the next time Git touches it

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (ft/branch)
$ git add test5.md

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (ft/branch)
$ git commit -m "feat: Implemented test 5"
[ft/branch c542877] feat: Implemented test 5
 1 file changed, 1 insertion(+)
 create mode 100644 test5.md

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (ft/branch)
$ git checkout dev
Switched to branch 'dev'

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git log --oneline ft/branch
c542877 (ft/branch) feat: Implemented test 5
8e6fe2d (origin/main, origin/HEAD, main) Initial commit

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git cherry-pick c542877
[dev 69b02eb] feat: Implemented test 5
 Date: Tue Sep 30 14:12:04 2025 +0200
 1 file changed, 1 insertion(+)
 create mode 100644 test5.md

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git log --oneline --graph
* 69b02eb (HEAD -> dev) feat: Implemented test 5
* 09200d9 chore: Create third and fourth files (added missing test4.md)    
* 248f285 chore: Create initial file
* 8e6fe2d (origin/main, origin/HEAD, main) Initial commit

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git reflog
69b02eb (HEAD -> dev) HEAD@{0}: cherry-pick: feat: Implemented test 5
09200d9 HEAD@{1}: checkout: moving from ft/branch to dev
c542877 (ft/branch) HEAD@{2}: commit: feat: Implemented test 5
8e6fe2d (origin/main, origin/HEAD, main) HEAD@{3}: checkout: moving from dev to ft/branch
09200d9 HEAD@{4}: rebase (abort): returning to refs/heads/dev
8e6fe2d (origin/main, origin/HEAD, main) HEAD@{5}: checkout: moving from 8e6fe2db5da8b47dbf41963b42817f39f2460db0 to ft/branch
8e6fe2d (origin/main, origin/HEAD, main) HEAD@{6}: rebase (start): checkout
 HEAD~2

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git push origin dev 
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 16 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (8/8), 745 bytes | 248.00 KiB/s, done.
Total 8 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), done.
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/elie-iradukunda/Gitexercises-2/pull/new/de 
remote:
To https://github.com/elie-iradukunda/Gitexercises-2.git
 * [new branch]      dev -> dev

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$



#part two commands

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git checkout -b ft/new-feature
Switched to a new branch 'ft/new-feature'

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (ft/new-feature)
$ echo "Core functionality for new feature" > feature.txt

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (ft/new-feature)
$ git add feature.txt
warning: in the working copy of 'feature.txt', LF will be replaced by CRLF the next time Git touches it

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (ft/new-feature)
$ git commit -m "Implemented core functionality for new feature"
[ft/new-feature d684934] Implemented core functionality for new feature
 1 file changed, 1 insertion(+)
 create mode 100644 feature.txt

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (ft/new-feature)
$ git checkout dev 
Switched to branch 'dev'

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ echo "Project introduction" > readme.txt

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git add readme.txt
warning: in the working copy of 'readme.txt', LF will be replaced by CRLF the next time Git touches it

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git commit -m "Updated project readme"
[dev 121f81f] Updated project readme
 1 file changed, 1 insertion(+)
 create mode 100644 readme.txt

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git push -u origin ft/new-feature
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 16 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 330 bytes | 330.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.       
remote:
remote: Create a pull request for 'ft/new-feature' on GitHub by visiting:  
remote:      https://github.com/elie-iradukunda/Gitexercises-2/pull/new/ft/new-feature
remote:
To https://github.com/elie-iradukunda/Gitexercises-2.git
 * [new branch]      ft/new-feature -> ft/new-feature
branch 'ft/new-feature' set up to track 'origin/ft/new-feature'.

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git branch -d ft/new-feature
warning: deleting branch 'ft/new-feature' that has been merged to
         'refs/remotes/origin/ft/new-feature', but not yet merged to HEAD  
Deleted branch ft/new-feature (was d684934).

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git push origin --delete ft/new-feature
To https://github.com/elie-iradukunda/Gitexercises-2.git
 - [deleted]         ft/new-feature

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git checkout -b ft/new-branch-from-commit HEAD~2
Switched to a new branch 'ft/new-branch-from-commit'

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (ft/new-branch-from-commit)
$ git checkout dev 
Switched to branch 'dev'

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git merge ft/new-branch-from-commit
Already up to date.

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git checkout ft/new-branch-from-commit
Switched to branch 'ft/new-branch-from-commit'

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (ft/new-branch-from-commit)
$ git rebase dev
Successfully rebased and updated refs/heads/ft/new-branch-from-commit.     

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (ft/new-branch-from-commit)
$ git branch -m ft/new-branch-from-commit ft/improved-branch-name

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (ft/improved-branch-name)
$ git log --oneline --graph
* 121f81f (HEAD -> ft/improved-branch-name, dev) Updated project readme
* 7dbbe06 (origin/dev) adding part one commands
* 69b02eb feat: Implemented test 5
* 09200d9 chore: Create third and fourth files (added missing test4.md)    
* 248f285 chore: Create initial file
* 8e6fe2d (origin/main, origin/HEAD, main) Initial commit

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (ft/improved-branch-name)
$ git checkout 69b02eb
Note: switching to '69b02eb'.

You are in 'detached HEAD' state. You can look around, make experimental   
changes and commit them, and you can discard any commits you make in this  
state without impacting any branches by switching back to a branch.        

If you want to create a new branch to retain commits you create, you may   
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 69b02eb feat: Implemented test 5

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 ((69b02eb...))
$ git status
HEAD detached at 69b02eb
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        test1.md

nothing added to commit but untracked files present (use "git add" to track)

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 ((69b02eb...))
$ git checkout -b ft/experimental-changes
Switched to a new branch 'ft/experimental-changes'

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (ft/experimental-changes)
$ git checkout ft/improved-branch-name
Switched to branch 'ft/improved-branch-name'

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (ft/improved-branch-name)
$ echo "Some experimental changes" > experiment.txt

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (ft/improved-branch-name)
$ git add experiment.txt
warning: in the working copy of 'experiment.txt', LF will be replaced by CRLF the next time Git touches it

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (ft/improved-branch-name)
$ git commit -m "Experiment in detached HEAD"
[ft/improved-branch-name db65f26] Experiment in detached HEAD
 1 file changed, 1 insertion(+)
 create mode 100644 experiment.txt

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (ft/improved-branch-name)
$ git checkout -b ft/experimental-changes
fatal: a branch named 'ft/experimental-changes' already exists

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (ft/improved-branch-name)
$ git checkout  ft/experimental-changes
Switched to branch 'ft/experimental-changes'

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (ft/experimental-changes)
$ git switch ft/improved-branch-name
Switched to branch 'ft/improved-branch-name'

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (ft/improved-branch-name)
$ git push -u origin ft/improved-branch-name
Enumerating objects: 19, done.
Counting objects: 100% (19/19), done.
Delta compression using up to 16 threads
Compressing objects: 100% (13/13), done.
Writing objects: 100% (17/17), 3.20 KiB | 468.00 KiB/s, done.
Total 17 (delta 5), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (5/5), done.
remote:
remote: Create a pull request for 'ft/improved-branch-name' on GitHub by visiting:
remote:      https://github.com/elie-iradukunda/Gitexercises-2/pull/new/ft/improved-branch-name
remote:
To https://github.com/elie-iradukunda/Gitexercises-2.git
 * [new branch]      ft/improved-branch-name -> ft/improved-branch-name    
branch 'ft/improved-branch-name' set up to track 'origin/ft/improved-branch-name'.

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (ft/improved-branch-name)
$ git checkout dev 
Switched to branch 'dev'

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git add .

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$ git commit -m"feat: added new functionality"
[dev e78faf9] feat: added new functionality
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test1.md

user@LAPTOP-V9PT987N MINGW64 ~/Desktop/githubexercises/Gitexercises-2 (dev)
$

```