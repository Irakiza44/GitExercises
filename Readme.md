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