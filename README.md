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
  ### Exercise 2
  ```bash
  
  ```