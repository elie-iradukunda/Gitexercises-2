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

```