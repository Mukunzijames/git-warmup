# git exercises
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git init
Initialized empty Git repository in C:/Users/Uwimpuhwe Honorine/Desktop/git-exercises/.git/
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git branch -M main
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git status
On branch main

nothing to commit (create/copy files and use "git add" to track)
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git add readme.md

No commits yet
Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   readme.md

PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git commit -m "git project"
[main (root-commit) 4ed6619] git project
 1 file changed, 3 insertions(+)
 create mode 100644 readme.md
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git status
On branch main
nothing to commit, working tree clean
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use


To have this happen automatically for branches without a tracking

PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises>  git push --set-upstream origin main   
Counting objects: 100% (3/3), done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Mukunzijames/git-warmup.git
error: failed to push some refs to 'https://github.com/Mukunzijames/git-warmup.git'
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises>     git push --set-upstream origin main
fatal: unable to access 'https://github.com/Mukunzijames/git-warmup.git/': Failed to connect to github.com port 443 after 21116 ms: Couldn't connect to server
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises>  git push --set-upstream origin main   
Everything up-to-date
branch 'main' set up to track 'origin/main'.
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git checkout -b dev
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git status
On branch dev
nothing to commit, working tree clean
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev
To have this happen automatically for branches without a tracking

PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git push --set-upstream origin dev
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/Mukunzijames/git-warmup/pull/new/dev
remote:
To https://github.com/Mukunzijames/git-warmup.git
 * [new branch]      dev -> dev
branch 'dev' set up to track 'origin/dev'.
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git checkout -b test
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git status
On branch test
nothing to commit, working tree clean
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git push 
fatal: The current branch test has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin test
To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises>  git push --set-upstream origin test
remote:
remote:      https://github.com/Mukunzijames/git-warmup/pull/new/test
To https://github.com/Mukunzijames/git-warmup.git
 * [new branch]      test -> test
Switched to branch 'dev'
Your branch is up to date with 'origin/dev'.
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git branch -d test
Deleted branch test (was 4ed6619).
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git push origin --delete test
fatal: unable to access 'https://github.com/Mukunzijames/git-warmup.git/': Could not resolve host: github.com
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git push origin --delete test
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git push origin --delete test
 - [deleted]         test
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html

Saved working directory and index state WIP on dev: 4ed6619 git project
stash@{0}: WIP on dev: 4ed6619 git project
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git add about.html
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git stash
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git stash list
stash@{1}: WIP on dev: 4ed6619 git project
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git add team.html
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git status
Your branch is up to date with 'origin/dev'.
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git stash
Saved working directory and index state WIP on dev: 4ed6619 git project
stash@{0}: WIP on dev: 4ed6619 git project
stash@{1}: WIP on dev: 4ed6619 git project
stash@{2}: WIP on dev: 4ed6619 git project
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git stash pop about.html
error: about.html is not a valid reference
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git stash pop stash@{1}
error: unknown switch `e'
usage: git stash pop [--index] [-q | --quiet] [<stash>]
    --index               attempt to recreate the index

PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git stash pop 
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
        new file:   team.html
Dropped refs/stash@{0} (870a5f83ff677ffd035fdeddbf1e435c74a9339e)
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git add team.html
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git status
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Saved working directory and index state WIP on dev: 4ed6619 git project
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git stash list
stash@{0}: WIP on dev: 4ed6619 git project
stash@{1}: WIP on dev: 4ed6619 git project
stash@{2}: WIP on dev: 4ed6619 git project
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git stash pop stash@{1}
usage: git stash pop [--index] [-q | --quiet] [<stash>]

    -q, --quiet           be quiet, only report errors
    --index               attempt to recreate the index

PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises>  git stash pop stash@{1}
error: unknown switch `e'
usage: git stash pop [--index] [-q | --quiet] [<stash>]

    -q, --quiet           be quiet, only report errors
    --index               attempt to recreate the index
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git stash list
stash@{0}: WIP on dev: 4ed6619 git project
stash@{1}: WIP on dev: 4ed6619 git project
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git stash pop stash@{1}
>>
error: unknown switch `e'
usage: git stash pop [--index] [-q | --quiet] [<stash>]
          
    -q, --quiet           be quiet, only report errors

PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git stash list
stash@{0}: WIP on dev: 4ed6619 git project
stash@{1}: WIP on dev: 4ed6619 git project
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git stash pop stash@{2}
error: unknown switch `e'
usage: git stash pop [--index] [-q | --quiet] [<stash>]

    -q, --quiet           be quiet, only report errors
    --index               attempt to recreate the index

PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git stash list
stash@{0}: WIP on dev: 4ed6619 git project
stash@{1}: WIP on dev: 4ed6619 git project
stash@{2}: WIP on dev: 4ed6619 git project
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git stash pop --index
>>   stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

  (use "git restore --staged <file>..." to unstage)
        new file:   team.html
stash@ : The term 'stash@' is not recognized as the name of a cmdlet, function, script file, or operable program. Check the spelling   
of the name, or if a path was included, verify that the path is correct and try again.
At line:2 char:3
+   stash@{1}
+   ~~~~~~
    + CategoryInfo          : ObjectNotFound: (stash@:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git stash list
stash@{1}: WIP on dev: 4ed6619 git project
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git add team.html
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git status
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git stash
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git stash list
stash@{0}: WIP on dev: 4ed6619 git project
stash@{1}: WIP on dev: 4ed6619 git project
stash@{2}: WIP on dev: 4ed6619 git project
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git stash pop --index stash@{1}
error: unknown switch `e'
usage: git stash pop [--index] [-q | --quiet] [<stash>]

    -q, --quiet           be quiet, only report errors
    --index               attempt to recreate the index

PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git stash pop --index
>> stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

  (use "git restore --staged <file>..." to unstage)

Dropped refs/stash@{0} (19612c4d0260a009ffd00e2b4cb95acf08c48287)
stash@ : The term 'stash@' is not recognized as the name of a cmdlet, function, script file, or operable program. Check the spelling   
of the name, or if a path was included, verify that the path is correct and try again.
At line:2 char:1
+ stash@{1}
+ ~~~~~~
    + CategoryInfo          : ObjectNotFound: (stash@:String) [], CommandNotFoundException
 
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git restore
git: 's' is not a git command. See 'git --help'.
The most similar commands are
        show
        status
        lfs
        svn
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git stash list
stash@{0}: WIP on dev: 4ed6619 git project
stash@{1}: WIP on dev: 4ed6619 git project
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git add team.html 
Saved working directory and index state WIP on dev: 4ed6619 git project
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git stash list
stash@{0}: WIP on dev: 4ed6619 git project
stash@{1}: WIP on dev: 4ed6619 git project
stash@{2}: WIP on dev: 4ed6619 git project
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git stash pop stash@{1}
error: unknown switch `e'
usage: git stash pop [--index] [-q | --quiet] [<stash>]
    -q, --quiet           be quiet, only report errors
    --index               attempt to recreate the index

PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git stash pop 1
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
Dropped refs/stash@{1} (206b516eee93859516e9f9234e2ccd9780016845)
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git stash pop 0
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git add team.html
On branch dev
Your branch is up to date with 'origin/dev'.
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   team.html

PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git stash team.html
fatal: subcommand wasn't specified; 'push' can't be assumed due to unexpected token 'team.html'
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git stash 
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git stash list
stash@{0}: WIP on dev: 4ed6619 git project
stash@{1}: WIP on dev: 4ed6619 git project
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git stash pop 1
On branch dev
Your branch is up to date with 'origin/dev'.

  (use "git restore --staged <file>..." to unstage)
        new file:   home.html

PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git status
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html

[dev 2a70938] home changes
 create mode 100644 home.html
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 487 bytes | 121.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Mukunzijames/git-warmup.git
stash@{0}: WIP on dev: 4ed6619 git project
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git stash pop
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   team.html

Dropped refs/stash@{0} (859cc4734c659e5fd4e4d663a32f54c801d49b9e)
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git reset
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises> git status
On branch dev
Your branch is up to date with 'origin/dev'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html
        team.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\Uwimpuhwe Honorine\Desktop\git-exercises>
this project of git exercises
