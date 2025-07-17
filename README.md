
# git-clone-exercise
# Gym-Git-Exercise-Solutions
## Bundle1
### Exercise1
```bash
 Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (main)
$ touch index.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (main)
$ git branch -M master

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (master)
$ git add .

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (master)
$ git commit -m "bubble1: creating a file and fill the content
"
[master b875379] bubble1: creating a file and fill the content
 1 file changed, 11 insertions(+)
 create mode 100644 index.html
 $ git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 458 bytes | 229.00 KiB/s, done.  
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0) 
To https://github.com/dieuaime-shami/Gym-Git-Exercise-Solutions.git
   9c0d739..b875379  main -> main
   $ git branch dev

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (main)
$ git checkout dev
M       README.md
Switched to branch 'dev'

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (dev)
$ git branch text

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (dev)
$ git branch 
* dev
  main
  text
Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (dev)
$ git push origin --delete text
To https://github.com/dieuaime-shami/Gym-Git-Exercise-Solutions.git
 - [deleted]         text

```
 ### Exercise2
 ```bash
  Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (main)
$ touch home.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (main)
$ git add home.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (main)
$ git stash push -m "home.html"
Saved working directory and index state On main: home.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (main)
$ touch about.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (main)
$ git stash push -m "about"
No local changes to save

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (main)
$ git add about.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (main)
$ git stash push -m "about.html"
Saved working directory and index state On main: about.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (main)
$ touch team.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (main)
$ git add team.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (main)
$ git stash push -m "team.html"    
Saved working directory and index state On main: team.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (main)
$ git stash lis
fatal: subcommand wasn't specified; 'push' can't be assumed due to unexpected token 'lis'

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (main)
$ git stash list
stash@{0}: On main: team.html
stash@{1}: On main: about.html     
stash@{2}: On main: home.html      
stash@{3}: WIP on main: b875379 bubble1: creating a file and fill the content

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (main)
$ git stash pop stash@{1}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html     

Dropped stash@{1} (1d492b6a68866e15e26df0392f7c7ccb33c18fb7)

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (main)
$ git stash pop stash@{2}:
fatal: 'stash@{2}:' is not a stash-like commit

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (main)
$ git stash pop stash@{1}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html     
        new file:   home.html      

Dropped stash@{1} (84decca143bf5883824eca8495053a84fe8f7b88)

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html     
        new file:   home.html      


Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (main)
$ git add .

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (main)
$ git commit -m "about and home"
[main 3527c9a] about and home
 2 files changed, 22 insertions(+) 
 create mode 100644 about.html     
 create mode 100644 home.html      

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (main)
$ git stash list
stash@{0}: On main: team.html
stash@{1}: WIP on main: b875379 bubble1: creating a file and fill the content

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (main)
$ git stash pop stash@{0}
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html      

Dropped stash@{0} (3ebd307f3fe7a7120cd3420a5f79f63960dd83a0)

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (main)
$ git reset --hard
HEAD is now at 3527c9a about and home
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean


 ```
(exercise 2)

 ## Bundle 2
 ```bash
$ git branch ft/bundle-2

Switched to branch 'ft/bundle-2'

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/bundle-2)       
$ touch services.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/bundle-2)       
$ git add services.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git commit -m "adding content to services"
[ft/bundle-2 bb09f1f] adding content to services
 1 file changed, 11 insertions(+)
 create mode 100644 services.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/bundle-2)       
$ git push origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 443 bytes | 443.00 KiB/s, done.  
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0) 
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
me-shami/Gym-Git-Exercise-Solutions/pull/new/ft/bundle-2      
remote:
To https://github.com/dieuaime-shami/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
 ```
  ### exercises2
  ```bash
  $ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (main)
$ git checkout main
Already on 'main'
Your branch is up to date with 'origin/main'.

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (main)
$ git pull origin main
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (1/1), 902 bytes | 128.00 KiB/s, done.
From https://github.com/dieuaime-shami/Gym-Git-Exercise-Solutions
 * branch            main       -> FETCH_HEAD
   1346196..2eeac7b  main       -> origin/main
Updating 1346196..2eeac7b
Fast-forward
 README.md     | 34 ++++++++++++++++++++++++++++++++--

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (main)
$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git add services.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git commit -m "redesign"
[ft/service-redesign 169c2fe] redesign
 1 file changed, 1 insertion(+)

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git push origin ft/services-redesign
error: src refspec ft/services-redesign does not match any
error: failed to push some refs to 'https://github.com/dieuaime-shami/Gym-Git-Exercise-Solutions.git'

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git push origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 303 bytes | 303.00 KiB/s, done.  
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0) 
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/dieuaime-shami/Gym-Git-Exercise-Solutions/pull/new/ft/service-redesign
remote:
To https://github.com/dieuaime-shami/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/service-redesign -> ft/service-redesign

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (main)
$ git add services.html
```
## Bundle 3
  ### exercise 1
  ```bash
  $ git branch ft/team-page

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ touch team.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git add team.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git commit -m "team.html"
[ft/service-redesign 055648a] team.html
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 team.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git switch ft/team-page
M       README.md
Switched to branch 'ft/team-page'

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/team-page)
$ git push origin -u
fatal: The current branch ft/team-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/team-page

To have this happen automatically for branches without a tracking        
upstream, see 'push.autoSetupRemote' in 'git help config'.


Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/team-page)
$ git push origin ft/team-page
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote: 
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:  
remote:      https://github.com/dieuaime-shami/Gym-Git-Exercise-Solutions/pull/new/ft/team-page
remote: 
To https://github.com/dieuaime-shami/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/team-page -> ft/team-page

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/team-page)
$ git switch main
error: Your local changes to the following files would be overwritten by checkout:
        README.md
Please commit your changes or stash them before you switch branches.     
Aborting

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/team-page)
$ git checkout main
error: Your local changes to the following files would be overwritten by checkout:
        README.md
Please commit your changes or stash them before you switch branches.     
Aborting

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/team-page)
$ git status
On branch ft/team-page
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)  
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")        

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/team-page)
$ git stash -u 
Saved working directory and index state WIP on ft/team-page: d2fdd13 read me

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/team-page)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (main)
$ git checkout -u ft/contact-page
error: unknown switch `u'
usage: git checkout [<options>] <branch>
   or: git checkout [<options>] [<branch>] -- <file>...

    -b <branch>           create and checkout a new branch
    -B <branch>           create/reset and checkout a branch
    -l                    create reflog for new branch
    --[no-]guess          second guess 'git checkout <no-such-branch>' (default)
    --[no-]overlay        use overlay mode (default)
    -q, --[no-]quiet      suppress progress reporting
    --[no-]recurse-submodules[=<checkout>]
                          control recursive updating of submodules       
    --[no-]progress       force progress reporting
    -m, --[no-]merge      perform a 3-way merge with the new branch      
    --[no-]conflict <style>
                          conflict style (merge, diff3, or zdiff3)       
    -d, --[no-]detach     detach HEAD at named commit
    -t, --[no-]track[=(direct|inherit)]
                          set branch tracking configuration
    -f, --[no-]force      force checkout (throw away local modifications)
    --[no-]orphan <new-branch>
                          new unborn branch
    --[no-]overwrite-ignore
                          update ignored files (default)
    --[no-]ignore-other-worktrees
                          do not check if another worktree is using this branch
    -2, --ours            checkout our version for unmerged files        
    -3, --theirs          checkout their version for unmerged files      
    -p, --[no-]patch      select hunks interactively
    --[no-]ignore-skip-worktree-bits
                          do not limit pathspecs to sparse entries only  
    --[no-]pathspec-from-file <file>
                          read pathspec from file
    --[no-]pathspec-file-nul
                          with --pathspec-from-file, pathspec elements are separated with NUL character


Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (main)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/team-page)
$ git log
commit d2fdd136fd6586b0513f968eab0501d32321f8f6 (HEAD -> ft/team-page, origin/ft/team-page, origin/ft/service-redesign)
Author: dieuaime-shami <shamidieuaime272@gmail.com>
Date:   Thu Jul 17 18:55:43 2025 +0200

    read me

commit 0e530a9d6cc22c639969da984dd991514b5c7dd5
Merge: 169c2fe bf9b71a
Author: dieuaime-shami <shamidieuaime272@gmail.com>
Date:   Thu Jul 17 18:42:34 2025 +0200


Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/team-page)
$ git log --oneline
d2fdd13 (HEAD -> ft/team-page, origin/ft/team-page, origin/ft/service-redesign) read me
0e530a9 Merge branch 'main' into ft/service-redesign
bf9b71a (origin/main, origin/HEAD, main, ft/contact-page) read me        
169c2fe redesign
2eeac7b Merge pull request #1 from dieuaime-shami/ft/bundle-2 done       
3cc3cd7 (origin/ft/bundle-2) updating readme content
bb09f1f adding content to services
1346196 exercise 2
3527c9a about and home
b875379 (origin/dev, dev) bubble1: creating a file and fill the content  
9c0d739 Initial commit

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/team-page)
$ git log --oneline --reverse
9c0d739 Initial commit
b875379 (origin/dev, dev) bubble1: creating a file and fill the content  
3527c9a about and home
1346196 exercise 2
bb09f1f adding content to services
3cc3cd7 (origin/ft/bundle-2) updating readme content
2eeac7b Merge pull request #1 from dieuaime-shami/ft/bundle-2 done       
169c2fe redesign
bf9b71a (origin/main, origin/HEAD, main, ft/contact-page) read me
0e530a9 Merge branch 'main' into ft/service-redesign
d2fdd13 (HEAD -> ft/team-page, origin/ft/team-page, origin/ft/service-redesign) read me

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/team-page)

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git cherry-pick d2fdd13
[ft/contact-page 7788476] read me
 Date: Thu Jul 17 18:55:43 2025 +0200
 1 file changed, 86 insertions(+)

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/contact-page)
$ ls
about.html  home.html  index.html  README.md  services.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git chechout ft/team-page
git: 'chechout' is not a git command. See 'git --help'.

The most similar command is
        checkout

Switched to branch 'ft/team-page'

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-SolutiSwitched to branch 'ft/team-page'

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/team-page)
$ ls
about.html  home.html  index.html  README.md  services.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/team-page)
$ touch team.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/team-page)
$ git add team.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/team-page)
$ git commit -m "add team page"
[ft/team-page 8467cba] add team page
 1 file changed, 11 insertions(+)
 create mode 100644 team.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/team-page)
$ git push origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 431 bytes | 431.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/dieuaime-shami/Gym-Git-Exercise-Solutions.git
   d2fdd13..8467cba  ft/team-page -> ft/team-page 

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git log --oneline --reverse
9c0d739 Initial commit
b875379 (origin/dev, dev) bubble1: creating a file and fill the content
3527c9a about and home
1346196 exercise 2
bb09f1f adding content to services
3cc3cd7 (origin/ft/bundle-2) updating readme content
2eeac7b Merge pull request #1 from dieuaime-shami/ft/bundle-2 done
bf9b71a (origin/main, origin/HEAD, main) read me
7788476 (HEAD -> ft/contact-page) read me

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/team-page)
$ git log --oneline --reverse
9c0d739 Initial commit
b875379 (origin/dev, dev) bubble1: creating a file and fill the content
3527c9a about and home
1346196 exercise 2
bb09f1f adding content to services
3cc3cd7 (origin/ft/bundle-2) updating readme content
2eeac7b Merge pull request #1 from dieuaime-shami/ft/bundle-2 done
169c2fe redesign
bf9b71a (origin/main, origin/HEAD, main) read me
0e530a9 Merge branch 'main' into ft/service-redesign
d2fdd13 (origin/ft/service-redesign) read me      
8467cba (HEAD -> ft/team-page, origin/ft/team-page) add team page

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git cherry-pick 8467cba
[ft/contact-page 2cc3ad5] add team page
 Date: Thu Jul 17 23:25:10 2025 +0200
 1 file changed, 11 insertions(+)
 create mode 100644 team.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git add team.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git commit -m "ft: add content"
[ft/contact-page 273b23d] ft: add content
 1 file changed, 3 insertions(+)

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git push origin ft/contact-page
Enumerating objects: 11, done.
Counting objects: 100% (11/11), done.
Delta compression using up to 12 threads
Compressing objects: 100% (9/9), done.
Writing objects: 100% (9/9), 1.39 KiB | 1.39 MiB/s, done.
Total 9 (delta 5), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (5/5), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/dieuaime-shami/Gym-Git-Exercise-Solutions/pull/new/ft/contact-page  
remote:
To https://github.com/dieuaime-shami/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/contact-page -> ft/contact-page

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/faq-page)
$ touch faq.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git commit -a-m "faq.html"
error: unknown option `m'
usage: git commit [-a | --interactive | --patch] [-s] [-v] [-u[<mode>]] [--amend]
                  [--dry-run] [(-c | -C | --squash) <commit> | --fixup [(amend|reword):]<commit>]   
                  [-F <file> | -m <msg>] [--reset-author] [--allow-empty]
                  [--allow-empty-message] [--no-verify] [-e] [--author=<author>]
                  [--date=<date>] [--cleanup=<mode>] [--[no-]status]
                  [-i | -o] [--pathspec-from-file=<file> [--pathspec-file-nul]]
                  [(--trailer <token>[(=|:)<value>])...] [-S[<keyid>]]
                  [--] [<pathspec>...]

    -q, --[no-]quiet      suppress summary after successful commit
    -v, --[no-]verbose    show diff in commit message template

Commit message options
    -F, --[no-]file <file>
                          read message from file  
    --[no-]author <author>
                          override author for commit
    --[no-]date <date>    override date for commit
    -m, --[no-]message <message>
                          commit message
    -c, --[no-]reedit-message <commit>
                          reuse and edit message from specified commit
    -C, --[no-]reuse-message <commit>
                          reuse message from specified commit
    --[no-]fixup [(amend|reword):]commit
                          use autosquash formatted message to fixup or amend/reword specified commit
    --[no-]squash <commit>
                          use autosquash formatted message to squash specified commit
    --[no-]reset-author   the commit is authored by me now (used with -C/-c/--amend)
    --trailer <trailer>   add custom trailer(s)   
    -s, --[no-]signoff    add a Signed-off-by trailer
    -t, --[no-]template <file>
                          use specified template file
    -e, --[no-]edit       force edit of commit    
    --[no-]cleanup <mode> how to strip spaces and #comments from message
    --[no-]status         include status in commit message template
    -S, --[no-]gpg-sign[=<key-id>]
                          GPG sign commit

Commit contents options
    -a, --[no-]all        commit all changed files
    -i, --[no-]include    add specified files to index for commit
    --[no-]interactive    interactively add files 
    -p, --[no-]patch      interactively add changes
    -o, --[no-]only       commit only specified files
    -n, --no-verify       bypass pre-commit and commit-msg hooks
    --verify              opposite of --no-verify 
    --[no-]dry-run        show what would be committed
    --[no-]short          show status concisely   
    --[no-]branch         show branch information 
    --[no-]ahead-behind   compute full ahead/behind values
    --[no-]porcelain      machine-readable output 
    --[no-]long           show status in long format (default)
    -z, --[no-]null       terminate entries with NUL
    --[no-]amend          amend previous commit   
    --no-post-rewrite     bypass post-rewrite hook
    --post-rewrite        opposite of --no-post-rewrite
    -u, --[no-]untracked-files[=<mode>]
                          show untracked files, optional modes: all, normal, no. (Default: all)     
    --[no-]pathspec-from-file <file>
                          read pathspec from file 
    --[no-]pathspec-file-nul
                          with --pathspec-from-file, pathspec elements are separated with NUL character


Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git commit -a -m "faq.html"
On branch ft/faq-page
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        faq.html

nothing added to commit but untracked files present (use "git add" to track)

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git add faq.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git commit -m "add faq.hmtl"
[ft/faq-page c35e370] add faq.hmtl
 1 file changed, 11 insertions(+)
 create mode 100644 faq.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git pus origin ft/faq-page
git: 'pus' is not a git command. See 'git --help'.

The most similar commands are
        push
        pull

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git push origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 428 bytes | 428.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/dieuaime-shami/Gym-Git-Exercise-Solutions/pull/new/ft/faq-page      
remote:
To https://github.com/dieuaime-shami/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/faq-page -> ft/faq-page   

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git log --oneline --reverse
9c0d739 Initial commit
b875379 (origin/dev, dev) bubble1: creating a file and fill the content
3527c9a about and home
1346196 exercise 2
bb09f1f adding content to services
3cc3cd7 (origin/ft/bundle-2) updating readme content
2eeac7b Merge pull request #1 from dieuaime-shami/ft/bundle-2 done
bf9b71a (origin/main, origin/HEAD, main) read me
7788476 read me
2cc3ad5 add team page
273b23d (origin/ft/contact-page, ft/contact-page) ft: add content
c35e370 (HEAD -> ft/faq-page, origin/ft/faq-page) add faq.hmtl

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git revet c35e370
git: 'revet' is not a git command. See 'git --help'.

The most similar command is
        revert

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git revert c35e370
hint: Waiting for your editor to close the file...
[ft/faq-page ce32493] Revert "add faq.hmtl"
 1 file changed, 11 deletions(-)
 delete mode 100644 faq.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git status
On branch ft/faq-page
nothing to commit, working tree clean

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git revert -h
usage: git revert [--[no-]edit] [-n] [-m <parent-number>] [-s] [-S[<keyid>]] <commit>...
   or: git revert (--continue | --skip | --abort | --quit)

    --quit                end revert or cherry-pick sequence
    --continue            resume revert or cherry-pick sequence
    --abort               cancel revert or cherry-pick sequence
    --skip                skip current commit and continue
    --[no-]cleanup <mode> how to strip spaces and #comments from message
    -n, --no-commit       don't automatically commit
    --commit              opposite of --no-commit 
    -e, --[no-]edit       edit the commit message 
    -s, --[no-]signoff    add a Signed-off-by trailer
    -m, --[no-]mainline <parent-number>
                          select mainline parent  
    --[no-]rerere-autoupdate
                          update the index with reused conflict resolution if possible
    --[no-]strategy <strategy>
                          merge strategy
    -X, --[no-]strategy-option <option>
                          option for merge strategy
    -S, --[no-]gpg-sign[=<key-id>]
                          GPG sign commit
    --[no-]reference      use the 'reference' format to refer to commits


Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git revert --abort 
error: no cherry-pick or revert in progress
fatal: revert failed

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git pick--abort 
git: 'pick--abort' is not a git command. See 'git --help'.

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git pick --abort 
git: 'pick' is not a git command. See 'git --help'.

The most similar command is
        pickaxe

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git revert --abort 
error: no cherry-pick or revert in progress
fatal: revert failed

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git status
On branch ft/faq-page
nothing to commit, working tree clean

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/faq-page)
$ ls
about.html  index.html  services.html
home.html   README.md   team.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/faq-page)
$ touch faq.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git rm faq.html
fatal: pathspec 'faq.html' did not match any files

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git rm
fatal: No pathspec was given. Which files should I remove?

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/faq-page)
$ rm faq.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git pull origin ft/faq-page
From https://github.com/dieuaime-shami/Gym-Git-Exercise-Solutions
 * branch            ft/faq-page -> FETCH_HEAD    
Already up to date.

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git status
On branch ft/faq-page
nothing to commit, working tree clean

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/faq-page)
$ ls
about.html  home.html   README.md      team.html
faq.html    index.html  services.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/team-page)
$ git revert --abort 
error: no cherry-pick or revert in progress
fatal: revert failed

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/team-page)
$ git revert c35e370
On branch ft/team-page
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        faq.html

nothing added to commit but untracked files present (use "git add" to track)

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/team-page)
$ git status
On branch ft/team-page
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        faq.html

nothing added to commit but untracked files present (use "git add" to track)

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/team-page)
$ git checkout ft/faq-page
Switched to branch 'ft/faq-page'

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git status
On branch ft/faq-page
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        faq.html

nothing added to commit but untracked files present (use "git add" to track)

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git add faq.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git status
On branch ft/faq-page
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   faq.html


Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git checkout ft/team-page
A       faq.html
Switched to branch 'ft/team-page'

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/team-page)
$ git status
On branch ft/team-page
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   faq.html


Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/team-page)
$ git checkout ft/faq-page
A       faq.html
Switched to branch 'ft/faq-page'

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git commit -m "add afaq file"
[ft/faq-page f086277] add afaq file
 1 file changed, 11 insertions(+)
 create mode 100644 faq.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/team-page)
$ git status
On branch ft/team-page
nothing to commit, working tree clean

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/team-page)
$ git log --oneline --reverse
9c0d739 Initial commit
b875379 (origin/dev, dev) bubble1: creating a file
 and fill the content
3527c9a about and home
1346196 exercise 2
bb09f1f adding content to services
3cc3cd7 (origin/ft/bundle-2) updating readme content
2eeac7b Merge pull request #1 from dieuaime-shami/ft/bundle-2 done
169c2fe redesign
bf9b71a (origin/main, origin/HEAD, main) read me
0e530a9 Merge branch 'main' into ft/service-redesign
d2fdd13 (origin/ft/service-redesign) read me      
8467cba (HEAD -> ft/team-page, origin/ft/team-page) add team page

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/team-page)
$ git revert 8467cba
hint: Waiting for your editor to close the file...
[ft/team-page 47d4d87] Revert "add team page"
 1 file changed, 11 deletions(-)
 delete mode 100644 team.html

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/team-page)
$ git push origin ft/team-page
B/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.     
To https://github.com/dieuaime-shami/Gym-Git-Exercise-Solutions.git      
   8467cba..47d4d87  ft/team-page -> ft/team-page

Shami dieu aime@SHAMI MINGW64 ~/Documents/thegyme/Gym Git Exercise Solutions/Gym-Git-Exercise-Solutions (ft/team-page)
$
```

