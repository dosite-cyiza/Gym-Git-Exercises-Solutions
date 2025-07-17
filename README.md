# Gym-Git-Exercises-Solutions

## Bundle 1

### Exercise 1

```bash
user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (main)
$ git checkout -b dev
Switched to a new branch 'dev'

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git status
On branch dev
nothing to commit, working tree clean

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git push origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions/pull/new/dev
remote:
To https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions.git
 * [new branch]      dev -> dev

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git checkout -b test
Switched to a new branch 'test'

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (test)
$ git push origin dev
Everything up-to-date

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (test)
$ git push origin test
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote: 
remote: Create a pull request for 'test' on GitHub by visiting:
remote:      https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions/pull/new/test
remote:
To https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions.git
 * [new branch]      test -> test

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (test)
$ git checkout dev
Switched to branch 'dev'

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git branch -D test
Deleted branch test (was 1dff6d7).

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git push origin --delete test
To https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions.git
 - [deleted]         test

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git log
commit 1dff6d726a9d7e624b9eee20cbdf65eebcffd5c6 (HEAD -> dev, origin/main, origin/dev, main)
Merge: 4f99b11 0e2978a
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 11:46:49 2025 +0200

    Merge branch 'main' of https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions

commit 4f99b11b64ff8c44eec908f5de41c24033cd8698
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 11:42:25 2025 +0200

    init project

commit 0e2978a5588c2647fd98428d1116c7848db99599
Author: Dosite Iradukunda Cyiza <145858744+dosite-cyiza@users.noreply.github.com>
Date:   Thu Jul 17 11:40:06 2025 +0200

    Initial commit
(END)
Date:   Thu Jul 17 11:42:25 2025 +0200

    init project

commit 0e2978a5588c2647fd98428d1116c7848db99599
Author: Dosite Iradukunda Cyiza <145858744+dosite-cyiza@users.noreply.github.com>
Date:   Thu Jul 17 11:40:06 2025 +0200

    Initial commit
(END)
commit 4f99b11b64ff8c44eec908f5de41c24033cd8698
Author: dosite-cyiza <dositecyiza@gmail.com>
commit 1dff6d726a9d7e624b9eee20cbdf65eebcffd5c6 (HEAD -> dev, origin/main, origin/dev, main)
Merge: 4f99b11 0e2978a
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 11:46:49 2025 +0200

    Merge branch 'main' of https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions

commit 4f99b11b64ff8c44eec908f5de41c24033cd8698
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 11:42:25 2025 +0200

    init project

commit 0e2978a5588c2647fd98428d1116c7848db99599
Author: Dosite Iradukunda Cyiza <145858744+dosite-cyiza@users.noreply.github.com>
Date:   Thu Jul 17 11:40:06 2025 +0200

    Initial commit

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git branch
* dev
  main

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git status
On branch dev
nothing to commit, working tree clean

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git remote
origin

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ Date:   Thu Jul 17 11:42:25 2025 +0200

    init project

commit 0e2978a5588c2647fd98428d1116c7848db99599
Author: Dosite Iradukunda Cyiza <145858744+dosite-cyiza@users.noreply.github.com>
Date:   Thu Jul 17 11:40:06 2025 +0200

    Initial commit


```
### Exercise 2
```bash
user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git stash list

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git add home.html

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git stash
Saved working directory and index state WIP on dev: 89bff22 setup

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git status
On branch dev
nothing to commit, working tree clean

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git stash list
stash@{0}: WIP on dev: 89bff22 setup

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git add about.html

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git stash
Saved working directory and index state WIP on dev: 89bff22 setup

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git stash list
stash@{0}: WIP on dev: 89bff22 setup
stash@{1}: WIP on dev: 89bff22 setup

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html

nothing added to commit but untracked files present (use "git add" to track)

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git add team.html

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git stash
Saved working directory and index state WIP on dev: 89bff22 setup

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git stash list
stash@{0}: WIP on dev: 89bff22 setup
stash@{1}: WIP on dev: 89bff22 setup
stash@{2}: WIP on dev: 89bff22 setup

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html

nothing added to commit but untracked files present (use "git add" to track)

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git stast pop stash@{1}
git: 'stast' is not a git command. See 'git --help'.

The most similar command is
        stash

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git stash pop stash@{1}
error: The following untracked working tree files would be overwritten by merge:
        about.html
Please move or remove them before you merge.
Aborting
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html
        team.html

nothing added to commit but untracked files present (use "git add" to track)
The stash entry is kept in case you need it again.

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git stash list
stash@{0}: WIP on dev: 89bff22 setup
stash@{1}: WIP on dev: 89bff22 setup
stash@{2}: WIP on dev: 89bff22 setup

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git stash pop stash@{1}
error: The following untracked working tree files would be overwritten by merge:
        about.html
Please move or remove them before you merge.
Aborting
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html
        team.html

nothing added to commit but untracked files present (use "git add" to track)
The stash entry is kept in case you need it again.

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ rm about.html

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ rm team.html

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git stash list
stash@{0}: WIP on dev: 89bff22 setup
stash@{1}: WIP on dev: 89bff22 setup
stash@{2}: WIP on dev: 89bff22 setup

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (9a77a886830003678b5641cffed9583e20dc2795)

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git status
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html


user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git stash list
stash@{0}: WIP on dev: 89bff22 setup
stash@{1}: WIP on dev: 89bff22 setup

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   home.html

Dropped stash@{1} (2452cc5c93b7ea9a1d9032e01f2054169e5738b9)

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git status
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   home.html


user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git commit add --all
fatal: paths 'add ...' with -a does not make sense

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git add --all

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git status
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        modified:   home.html


user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git commit -m "setup home and about pages"
[dev 57f9484] setup home and about pages
 2 files changed, 1 insertion(+), 1 deletion(-)
 create mode 100644 about.html

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git push origin dev
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 364 bytes | 364.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions.git
   89bff22..57f9484  dev -> dev

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git stash list
stash@{0}: WIP on dev: 89bff22 setup

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git stash pop stash@{0}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (c646524b2b02110b47d66327e8e67050a9b4a07e)

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git reset --hard
HEAD is now at 57f9484 setup home and about pages

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$

```

## Bundle 2

### Exercise 1

```bash

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (ft/bundle-2)
$ git touch services.html
git: 'touch' is not a git command. See 'git --help'.

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (ft/bundle-2)
$  touch services.html

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (ft/bundle-2)
$ git add services.html

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (ft/bundle-2)
$ git commit -m"setup services page"
[ft/bundle-2 f2b24d1] setup services page
 1 file changed, 12 insertions(+)
 create mode 100644 services.html

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (ft/bundle-2)
$ git push origin ft/bundle-2
fatal: unable to access 'https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions.git/': Could not resolve host: github.com

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (ft/bundle-2)
$ git push origin ft/bundle-2
fatal: unable to access 'https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions.git/': Could not resolve host: github.com

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (ft/bundle-2)
$ git push origin ft/bundle-2
fatal: unable to access 'https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions.git/': Could not resolve host: github.com

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (ft/bundle-2)
$ git push origin ft/bundle-2
fatal: unable to access 'https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions.git/': Could not resolve host: github.com

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (ft/bundle-2)
$ git push origin ft/bundle-2
fatal: unable to access 'https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions.git/': Could not resolve host: github.com

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (ft/bundle-2)
$ git push origin ft/bundle-2
fatal: unable to access 'https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions.git/': Could not resolve host: github.com

user@Dosite-Cyiza-Laptop MINGW64 /e/downloads/Exercises/Gym-Git-Exercises-Solutions (ft/bundle-2)
$ git push origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 438 bytes | 438.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions/pull/new/ft/bundle-2
remote:
To https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2

```
