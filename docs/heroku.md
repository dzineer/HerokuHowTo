Using Heroku & Heroku Commands
==================================

# replace REPLACE_ME_OS/REPLACE_ME_ARCH with values as noted below
$ wget https://cli-assets.heroku.com/heroku-cli/channels/stable/heroku-cli-REPLACEME_OS-REPLACE_ME_ARCH.tar.gz -O heroku.tar.gz
$ tar -xvzf heroku.tar.gz
$ mkdir -p /usr/local/lib /usr/local/bin
$ mv heroku-cli-v6.x.x-darwin-64 /usr/local/lib/heroku
$ ln -s /usr/local/lib/heroku/bin/heroku /usr/local/bin/heroku

```
Where REPLACE_ME_OS is one of "linux", "darwin", "windows" and REPLACE_ME_ARCH is one of "x64" or "x86" You also must replace "6.x.x" with the actual version.
```

```
wget https://cli-assets.heroku.com/heroku-cli/channels/stable/heroku-cli-windows-x64.tar.gz -O heroku.tar.gz
$ tar -xvzf heroku.tar.gz
$ mkdir -p /usr/local/lib /usr/local/bin
$ mv heroku-cli-v6.12.0-a504409-windows-x64 /usr/local/lib/heroku
$ ln -s /usr/local/lib/heroku/bin/heroku /usr/local/bin/heroku
```

I:\Projects\Jade_and_me\frank\projects\2017\HerokuHowTo>heroku login
Enter your Heroku credentials:
Email: frank@dzineer.com
Password: *********
Logged in as frank@dzineer.com

I:\Projects\Jade_and_me\frank\projects\2017\HerokuHowTo>heroku auth:whoami
frank@dzineer.com


Add a new project to the GitHub repository.
-------------------------------------------
After adding new repository to GitHub You will see this

create a new repository on the command line

```
echo "# HerokuHowTo" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin git@github.com:dzineer/HerokuHowTo.git
git push -u origin master
```

…or push an existing repository from the command line

```
git remote add origin git@github.com:dzineer/HerokuHowTo.git
git push -u origin master
```

Add new remote branch to repository
-----------------------------------

```
git remote add origin git@github.com:dzineer/GithubHowTo.git
```

Confirm git remote was added successfully
-----------------------------------------

```
$ git remote -v
origin  git@github.com:dzineer/GithubHowTo.git (fetch)
origin  git@github.com:dzineer/GithubHowTo.git (push)
```


Display our git remote branch
-----------------------------

```
$ git branch
* master
```

Push our local repository to GitHub remote
------------------------------------------

```
$ git push -u origin master
Counting objects: 15, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (13/13), done.
Writing objects: 100% (15/15), 2.91 KiB | 0 bytes/s, done.
Total 15 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), done.
To github.com:dzineer/GithubHowTo.git
 * [new branch]      master -> master
Branch master set up to track remote branch master from origin.
```

Okay what if we make changes ?
------------------------------
Change readme.md file to add author

Get the status

```
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   docs/github.md
        modified:   reame.md

no changes added to commit (use "git add" and/or "git commit -a")
```

Commit changes

```
$ git commit -a -m 'Added Author'
[master 48caf4f] Added Author
 2 files changed, 82 insertions(+), 7 deletions(-)
```

Add the changes to Github
---------------------

```
$ git push
Counting objects: 5, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 1.75 KiB | 0 bytes/s, done.
Total 5 (delta 0), reused 0 (delta 0)
To github.com:dzineer/GithubHowTo.git
   d2377e7..48caf4f  master -> master
```
git push again to confirm

```
$ git push
Everything up-to-date
```

Get the status again

```
$ git status
On branch master

Your branch is up-to-date with 'origin/master'.
nothing to commit, working tree clean
```

git push again to confirm

```
$ git push
Everything up-to-date
```
