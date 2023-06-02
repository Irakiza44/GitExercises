# GIT EXERCISES

## Bundle 1

### Exercise 1
```bash
Initialized empty Git repository in C:/Users/Didier/Desktop/Git Exercises/.git/
PS C:\Users\Didier\Desktop\Git Exercises> git status
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)
PS C:\Users\Didier\Desktop\Git Exercises> git branch -M main
PS C:\Users\Didier\Desktop\Git Exercises> git status
On branch main

No commits yet

nothing to commit (create/copy files and use "git add" to track)

PS C:\Users\Didier\Desktop\Git Exercises> git status
No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Readme.md

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\Didier\Desktop\Git Exercises> git add Readme.md
PS C:\Users\Didier\Desktop\Git Exercises> git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   Readme.md

PS C:\Users\Didier\Desktop\Git Exercises> git commit -m "my first commit to the project"
[main (root-commit) add1bae] my first commit to the project
 1 file changed, 22 insertions(+)
 create mode 100644 Readme.md
PS C:\Users\Didier\Desktop\Git Exercises> git remote add origin https://github.com/Irakiza44/GitExercises.git
PS C:\Users\Didier\Desktop\Git Exercises> git push -u origin main
Counting objects: 100% (3/3), done.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 450 bytes | 150.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Irakiza44/GitExercises.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
PS C:\Users\Didier\Desktop\Git Exercises> git checkout -b dev
Switched to a new branch 'dev'
PS C:\Users\Didier\Desktop\Git Exercises> git status
On branch dev
nothing to commit, working tree clean

remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/Irakiza44/GitExercises/pull/new/dev
remote:
To https://github.com/Irakiza44/GitExercises.git
 * [new branch]      dev -> dev
branch 'dev' set up to track 'origin/dev'.
PS C:\Users\Didier\Desktop\Git Exercises> git checkout -b test
Switched to a new branch 'test'
PS C:\Users\Didier\Desktop\Git Exercises> git branch
  dev
  main
* test

PS C:\Users\Didier\Desktop\Git Exercises> git push origin test
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'test' on GitHub by visiting:
remote:      https://github.com/Irakiza44/GitExercises/pull/new/test
remote:
To https://github.com/Irakiza44/GitExercises.git
 * [new branch]      test -> test

PS C:\Users\Didier\Desktop\Git Exercises> git checkout dev
Switched to branch 'dev'
Your branch is up to date with 'origin/dev'.
PS C:\Users\Didier\Desktop\Git Exercises> git branch
* dev
  main
  test

PS C:\Users\Didier\Desktop\Git Exercises> git branch -D test
Deleted branch test (was add1bae).
PS C:\Users\Didier\Desktop\Git Exercises> git push origin --delete test
To https://github.com/Irakiza44/GitExercises.git
 - [deleted]         test

```


### Exercise 2
```bash
PS C:\Users\Didier\Desktop\Git Exercises> git stash list
PS C:\Users\Didier\Desktop\Git Exercises> git add Home.html
PS C:\Users\Didier\Desktop\Git Exercises> git stash
Saved working directory and index state WIP on dev: 4f447fb my first commit to the project
On branch dev

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        About.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\Didier\Desktop\Git Exercises> git add About
fatal: pathspec 'About' did not match any files
PS C:\Users\Didier\Desktop\Git Exercises> git add About.html

PS C:\Users\Didier\Desktop\Git Exercises> git stash
Saved working directory and index state WIP on dev: 4f447fb my first commit to the project
PS C:\Users\Didier\Desktop\Git Exercises> git stash list
stash@{0}: WIP on dev: 4f447fb my first commit to the project
stash@{1}: WIP on dev: 4f447fb my first commit to the project

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Team.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\Didier\Desktop\Git Exercises> git add Team.html
PS C:\Users\Didier\Desktop\Git Exercises> git stash
Saved working directory and index state WIP on dev: 4f447fb my first commit to the project

PS C:\Users\Didier\Desktop\Git Exercises> git stash list
stash@{0}: WIP on dev: 4f447fb my first commit to the project
stash@{1}: WIP on dev: 4f447fb my first commit to the project
stash@{2}: WIP on dev: 4f447fb my first commit to the project

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (dev)
$ git stash pop stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   About.html

Dropped stash@{1} (4ba2a8a7574dd1422381e9c22d8b733e6a8d0231)

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (dev)
$ git stash pop stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   About.html
        new file:   Home.html

Dropped stash@{1} (6665fa44f1fc69dc3e56d49ecb81fcb3282b6879)

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (dev)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 579 bytes | 115.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/Irakiza44/GitExercises.git
   4f447fb..a863758  dev -> dev

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (dev)
$ git stash list
stash@{0}: WIP on dev: 4f447fb my first commit to the project

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (dev)
$ git stash pop stash@{0}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   Team.html

Dropped stash@{0} (242b27dbd48269e30d23384c24eef6fa04c9d6be)

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (dev)
$ git reset --hard
HEAD is now at a863758 stup my project with stashes

```
## Bundle 3
### Exercise 1
```bash

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (main)
$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/team-page)
$ git add team.html

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/team-page)
$ git status
On branch ft/team-page
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html


Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/team-page)
$ git commit -m "adding a new team page in the project"
[ft/team-page 9f6e408] adding a new team page in the project
 1 file changed, 12 insertions(+)
 create mode 100644 team.html

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/team-page)
$ git push
fatal: The current branch ft/team-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/team-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/team-page)
$ git push --set-upstream origin ft/team-page~
fatal: invalid refspec 'ft/team-page~'

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/team-page)
$ git push --set-upstream origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 493 bytes | 246.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/Irakiza44/GitExercises/pull/new/ft/team-page
remote:
To https://github.com/Irakiza44/GitExercises.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/team-page)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (main)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/contact-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/team-page)
$ git log
commit 9f6e4083c610262396d0de0020f30cccd5cf0258 (HEAD -> ft/team-page, origin/ft/team-page)Author: Your Name <you@example.com>
Date:   Fri Jun 2 16:25:09 2023 +0200

    adding a new team page in the project
commit 9f6e4083c610262396d0de0020f30cccd5cf0258 (HEAD -> ft/team-page, origin/ft/team-page)Author: Your Name <you@example.com>
Date:   Fri Jun 2 16:25:09 2023 +0200

    adding a new team page in the project

commit 6759643a39a537756011ff75ad77c4d2df497044 (origin/main, main, ft/contact-page)       



Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/contact-page)
$ git cherry-pick 9f6e4083c610262396d0de0020f30cccd5cf0258
[ft/contact-page 0defe39] adding a new team page in the project
 Date: Fri Jun 2 16:25:09 2023 +0200
 1 file changed, 12 insertions(+)
 create mode 100644 team.html

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/contact-page)
$ git log
commit 0defe399795bf3427e7fc78c1a66aac0bd41235b (HEAD -> ft/contact-page)
Author: Your Name <you@example.com>
Date:   Fri Jun 2 16:25:09 2023 +0200

    adding a new team page in the project

commit 6759643a39a537756011ff75ad77c4d2df497044 (origin/main, main)
:

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/contact-page)
$ git status
On branch ft/contact-page
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        contact.html

nothing added to commit but untracked files present (use "git add" to track)

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/contact-page)
$ git add .

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/contact-page)
$ git commit -m "adding changes to contact page"
[ft/contact-page c9ca952] adding changes to contact page
 1 file changed, 12 insertions(+)
 create mode 100644 contact.html

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/contact-page)
$ git push
fatal: The current branch ft/contact-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/contact-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/contact-page)
$ git push --set-upstream origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 750 bytes | 125.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/Irakiza44/GitExercises/pull/new/ft/contact-page
remote:
To https://github.com/Irakiza44/GitExercises.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/contact-page)
$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/faq-page)
$ git add .

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/faq-page)
$ git commit -m "adding new faq page to the project"
[ft/faq-page 2ad7670] adding new faq page to the project
 1 file changed, 12 insertions(+)
 create mode 100644 faq.html

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/faq-page)
$ git push
fatal: The current branch ft/faq-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/faq-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/faq-page)
$ git push --set-upstream origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 486 bytes | 486.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/Irakiza44/GitExercises/pull/new/ft/faq-page
remote:
To https://github.com/Irakiza44/GitExercises.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/faq-page)
$ git log
commit 2ad76707be0ebb9f9f00f82f2201fe678d024462 (HEAD -> ft/faq-page, origin/ft/faq-page)
Author: Your Name <you@example.com>
Date:   Fri Jun 2 16:55:03 2023 +0200

    adding new faq page to the project

commit c9ca952d9d183c4e3d2c367514a37e21ef09113d (origin/ft/contact-page, ft/contact-page)  
Author: Your Name <you@example.com>
Date:   Fri Jun 2 16:50:17 2023 +0200

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/faq-page)
$ git revert 2ad76707be0ebb9f9f00f82f2201fe678d0244621~
fatal: bad revision '2ad76707be0ebb9f9f00f82f2201fe678d0244621~'

Revert "adding changes to contact page"

This reverts commit c9ca952d9d183c4e3d2c367514a37e21ef09113d.

# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
#
# On branch ft/faq-page
# Your branch is up to date with 'origin/ft/faq-page'.
.git/COMMIT_EDITMSG [unix] (17:01 02/06/2023)                                       1,1 Top
"~/Desktop/Git Exercises/.git/COMMIT_EDITMSG" [unix] 13L, 378B 

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/faq-page)
$ git revert c9ca952d9d183c4e3d2c367514a37e21ef09113d
[ft/faq-page 06fcdc4] Revert "adding changes to contact page"
 1 file changed, 12 deletions(-)
 delete mode 100644 contact.htm

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/faq-page)
$ git log
commit 06fcdc46f341768367f8d5a76edd674bef9e2632 (HEAD -> ft/faq-page)
Author: Your Name <you@example.com>
Date:   Fri Jun 2 17:01:10 2023 +0200

    Revert "adding changes to contact page"

    This reverts commit c9ca952d9d183c4e3d2c367514a37e21ef09113d.

commit 2ad76707be0ebb9f9f00f82f2201fe678d024462 (origin/ft/faq-page)
Author: Your Name <you@example.com>

```