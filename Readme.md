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

## Bundle 2

### Exercise 1
```bash
Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (dev)
$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/bundle-2)
$ git status
On branch ft/bundle-2
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Service.html

nothing added to commit but untracked files present (use "git add" to track)

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/bundle-2)
$ git add Service.html

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/bundle-2)
$ git stash
Saved working directory and index state WIP on ft/bundle-2: 4b57721 stup my project with stashes

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/bundle-2)
$ git stash list
stash@{0}: WIP on ft/bundle-2: 4b57721 stup my project with stashes

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/bundle-2)
$ git stash pop stash@{0}
On branch ft/bundle-2
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   Service.html

Dropped stash@{0} (c6b65db621041b01f8b6100aa349e2964263e8b8)

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/bundle-2)
$ git status
On branch ft/bundle-2
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   Service.html


Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/bundle-2)
$ git commit -m "Creation of Service page in Our Project"
[ft/bundle-2 8ddb706] Creation of Service page in Our Project
 1 file changed, 12 insertions(+)
 create mode 100644 Service.html

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/bundle-2)
$ git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

Didier@DESKTOP-CUJ952O MINGW64 ~/Desktop/Git Exercises (ft/bundle-2)
$ git push --set-upstream origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 502 bytes | 167.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/Irakiza44/GitExercises/pull/new/ft/bundle-2
remote:
To https://github.com/Irakiza44/GitExercises.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.
```