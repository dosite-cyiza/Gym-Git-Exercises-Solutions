Git Exercises solutions

## Bundle 1

### Exercise 1

```bash

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (main)
$ git checkout -b dev
Switched to a new branch 'dev'

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git checkout -b test
Switched to a new branch 'test'

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (test)
$ git checkout dev
Switched to branch 'dev'

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git status
On branch dev
nothing to commit, working tree clean

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git push origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions/pull/new/dev
remote:
To https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions.git
 * [new branch]      dev -> dev

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git checkout test
Switched to branch 'test'

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (test)
$ git push origin test
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote: 
remote: Create a pull request for 'test' on GitHub by visiting:
remote:      https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions/pull/new/test
remote:
To https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions.git
 * [new branch]      test -> test

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (test)
$ git checkout dev
Switched to branch 'dev'

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git push origin --delete test
To https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions.git
 - [deleted]         test


```

### Exercise 2
``` bash
user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ touch home.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

nothing added to commit but untracked files present (use "git add" to track)

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git stash
No local changes to save

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git add home.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git stash
Saved working directory and index state WIP on dev: 383bc5a Bundle1 Exercise 1

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git stash list
stash@{0}: WIP on dev: 383bc5a Bundle1 Exercise 1

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ touch about.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git add about.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git stash
Saved working directory and index state WIP on dev: 383bc5a Bundle1 Exercise 1

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ touch team.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git add team.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git stash
Saved working directory and index state WIP on dev: 383bc5a Bundle1 Exercise 1

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git stash list
stash@{0}: WIP on dev: 383bc5a Bundle1 Exercise 1
stash@{1}: WIP on dev: 383bc5a Bundle1 Exercise 1
stash@{2}: WIP on dev: 383bc5a Bundle1 Exercise 1

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
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

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (1acd936bc58365895adca999e6ac14cdfdc867dc)

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git stash list
stash@{0}: WIP on dev: 383bc5a Bundle1 Exercise 1
stash@{1}: WIP on dev: 383bc5a Bundle1 Exercise 1

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (3676ff6d5f3a14c5bb3e2dc145528476f2ec3616)

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git add about.html,home.html
fatal: pathspec 'about.html,home.html' did not match any files

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git add about.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git add home.hmtl
fatal: pathspec 'home.hmtl' did not match any files

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git add home.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git commit -m"setup project"
[dev 5dc96d8] setup project
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 about.html
 create mode 100644 home.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git push origin dev
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 16 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 287 bytes | 287.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions.git
   383bc5a..5dc96d8  dev -> dev

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git stash list
stash@{0}: WIP on dev: 383bc5a Bundle1 Exercise 1

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git stash pop stash@{0}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   about.html
        modified:   home.html

Dropped stash@{0} (f2fc37ef0f378a8de2506438c096de3209ffaa18)

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git status
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   about.html
        modified:   home.html


user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git log
commit 5dc96d824ee5bbf646aee9c537ef0f0995687c2c (HEAD -> dev, origin/dev)
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sat Jul 19 19:24:35 2025 +0200

    setup project

commit 383bc5a666bd2d41f4b1e3c91264bf0161ee5ea1
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sat Jul 19 19:08:50 2025 +0200

    Bundle1 Exercise 1

commit 55e0a8c99d4a5a3148727324a4043586cb320e0d (origin/main, test, main)
Merge: 0f046d0 8c91da7
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sat Jul 19 18:58:29 2025 +0200

    Merge branch 'main' of https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions

commit 0f046d0aca3eaf46fe54096c0aa64571501b603a
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sat Jul 19 18:54:18 2025 +0200

    initial commit

commit 8fe41212521f711950bd06634d05df58a7e54869
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sat Jul 19 18:50:36 2025 +0200

    initial commit

commit 8c91da71c66aea8aa3e21076c5031b4475799a50
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sat Jul 19 18:34:47 2025 +0200

    remove all files

commit 68c54a7c0ec80042a01bc1e79863e0e51855baa9
Merge: bdda67d cab0620
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 19:04:20 2025 +0200

    Merge branch 'main' of https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions

commit bdda67d1efce817cee966cf06d4299653dae03d4
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 19:02:48 2025 +0200

    Bundle 2 Exercise 2

commit cab0620a2a8b0c03119bc681b1e76da5adc19c01
Merge: 05b64e5 775a9a0
Author: Dosite Iradukunda Cyiza <145858744+dosite-cyiza@users.noreply.github.com>
Date:   Thu Jul 17 18:58:27 2025 +0200

    Merge pull request #3 from dosite-cyiza/ft/service-redesign

    New File service.html

commit 775a9a095176954eb8ac12ecb0ce8de70f66128b
Merge: a880587 05b64e5
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 18:47:23 2025 +0200

    new changes in services.html

commit 05b64e5ad8913e1107fc9f32a87940a2065e45d5
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 18:23:37 2025 +0200

    adding new changes in services html

commit a880587b9e3899533ec5b2c1e4f8d31b858b1a95
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 18:20:30 2025 +0200

    new changes in file

commit 249a54f7b633d89fe27e2c91fc88cbce78c570e7
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 18:17:38 2025 +0200

    New File service.html

commit c856ff32b5642e3a38e447a094613ce806b2e022
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 18:02:33 2025 +0200

    bundle 2 Exercise 1 Terminal history

commit c48af74283d04186b9ab324664e92cad936ab8e7
Merge: 8882c8c f2b24d1
Author: Dosite Iradukunda Cyiza <145858744+dosite-cyiza@users.noreply.github.com>
Date:   Thu Jul 17 17:50:06 2025 +0200

    Merge pull request #1 from dosite-cyiza/ft/bundle-2

    Ft/bundle 2

commit 8882c8c6bb70cbe745cdcfb69fdf3659a016b46b
Merge: 1dff6d7 5b2770b
Author: Dosite Iradukunda Cyiza <145858744+dosite-cyiza@users.noreply.github.com>
Date:   Thu Jul 17 16:40:55 2025 +0200

    Merge pull request #2 from dosite-cyiza/dev

    Adding Bundle1- Exercise 2

commit 5b2770bdfb50f795024ceb91468aeb41aef2e6f8
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 16:36:54 2025 +0200

    terminal history ##bunde 1 exercise 1

commit f2b24d113cc8d81337222bd02debfdf67e764ddb
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 15:45:11 2025 +0200

    setup services page

commit 57f9484a719ca4f28ebf6043893158cb6b643126
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 15:17:58 2025 +0200

    setup home and about pages

commit 89bff22d1bf557665336722c165ddc62ddb3d0f3
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 13:01:26 2025 +0200

    setup

commit fad816e7815c11147eba477140cde57cabe3e787
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 12:19:55 2025 +0200

    Bunde1 Exercise 1

commit 1dff6d726a9d7e624b9eee20cbdf65eebcffd5c6
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

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git reset --hard 5dc96d824ee5bbf646aee9c537ef0f0995687c2c
HEAD is now at 5dc96d8 setup project

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$
```

## Bundle 2

### Exercise 1

``` bash 

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (dev)
$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/bundle-2)
$ touch services.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/bundle-2)
$ git add services.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/bundle-2)
$ git commit -m"feat: services.html"
[ft/bundle-2 40f5967] feat: services.html
 1 file changed, 12 insertions(+)
 create mode 100644 services.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/bundle-2)
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

### Exercise 2

```bash

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/service-redesign)
$ git pull origin main
From https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions
 * branch            main       -> FETCH_HEAD
Updating 55e0a8c..9022fc3
Fast-forward
 README.md     | 421 +++++++++++++++++++++++++++++++++++++++++++++++++++++++++-
 about.html    |   0
 home.html     |   0
 services.html |  12 ++
 4 files changed, 432 insertions(+), 1 deletion(-)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 services.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/service-redesign)
$ git add services.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/service-redesign)
$ git commit -m"feat: service-redesign"
On branch ft/service-redesign
nothing to commit, working tree clean

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/service-redesign)
$ git commit -m"feat: service-redesign"
On branch ft/service-redesign
nothing to commit, working tree clean

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/service-redesign)
$ git add services.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/service-redesign)
$ git commit -m"ft/service-redesign"
[ft/service-redesign 3db4be5] ft/service-redesign
 1 file changed, 6 insertions(+)

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/service-redesign)
$ git push origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 355 bytes | 355.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions/pull/new/ft/service-redesign
remote:
To https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions.git
 * [new branch]      ft/service-redesign -> ft/service-redesign

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/service-redesign)
$ git checkout main
Switched to branch 'main'

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (main)
$ git add services.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (main)
$ git commit -m"new changes in services page"
[main 49e0c03] new changes in services page
 1 file changed, 6 insertions(+)

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (main)
$ git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 359 bytes | 359.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions.git
   9022fc3..49e0c03  main -> main

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (main)
$ git checkout ft/service-redesign
error: Your local changes to the following files would be overwritten by checkout:
        services.html
Please commit your changes or stash them before you switch branches.
Aborting

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (main)
$ git add services.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (main)
$ git commit -m"new changes in services page"
[main a8c030e] new changes in services page
 1 file changed, 1 insertion(+), 1 deletion(-)
user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (main)
$ git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 296 bytes | 296.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions.git
   49e0c03..a8c030e  main -> main

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (main)
$ git checkout ft/services-redesign
error: pathspec 'ft/services-redesign' did not match any file(s) known to git

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/service-redesign)
$ git merge main
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/service-redesign|MERGING)
$ git add services.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/service-redesign)
$ git commit -m"resolve conflict"
On branch ft/service-redesign
nothing to commit, working tree clean
user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/service-redesign)
$ git push origin ft/service-redesign
Enumerating objects: 1, done.
Counting objects: 100% (1/1), done.
Writing objects: 100% (1/1), 239 bytes | 239.00 KiB/s, done.
Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions.git
   3db4be5..142399e  ft/service-redesign -> ft/service-redesign

```


## Bundle 3

### Exercise 1

```bash

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (main)
$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/team-page)
$ touch team.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/team-page)
$ git add team.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/team-page)
$ git commit -m"feat: team page"
[ft/team-page 7fe683f] feat: team page
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 team.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/team-page)
$ git push origin ft/team-page
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 16 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 237 bytes | 237.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions/pull/new/ft/team-page
remote:
To https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions.git
 * [new branch]      ft/team-page -> ft/team-page

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/team-page)
$ git add team.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/team-page)
$ git commit -m"feat: team page"
[ft/team-page 88587bb] feat: team page
 1 file changed, 11 insertions(+)

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/team-page)
$ git push origin ft/team-page
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 409 bytes | 409.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions.git
   7fe683f..88587bb  ft/team-page -> ft/team-page

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/team-page)
$ git checkout main
Switched to branch 'main'

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (main)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/contact-page)
$ touch contact.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/contact-page)
$ git add contact.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/contact-page)
$ git commit -m"feat: contact page"
[ft/contact-page 61c7b53] feat: contact page
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 contact.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/contact-page)
$ git push origin ft/contact-page
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 16 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 233 bytes | 233.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions/pull/new/ft/contact-page
remote:
To https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions.git
 * [new branch]      ft/contact-page -> ft/contact-page

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/contact-page)
$ git add contact.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/contact-page)
$ git commit -m"feat: contact page"
[ft/contact-page 253ffbc] feat: contact page
 1 file changed, 11 insertions(+)

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/contact-page)
$ git push origin ft/contact-page
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 431 bytes | 431.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions.git
   61c7b53..253ffbc  ft/contact-page -> ft/contact-page

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/contact-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/team-page)
$ git log
commit 88587bb0fb1fcd95d7c1d746d942f2e28c0afbae (HEAD -> ft/team-page, origin/ft/team-page)
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sun Jul 20 17:38:12 2025 +0200

    feat: team page

commit 7fe683f9d35977c782d828325806134e8f26a6b6
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sun Jul 20 17:37:20 2025 +0200

    feat: team page

commit df76fa9997c6de6ce3bd50dc7769aae34e6eb33f (origin/main, main)
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sun Jul 20 14:24:20 2025 +0200

    Bundle 2 Exercise 2

commit def696f8e637e34fe33517e93f3f48be90503ba9
Merge: a8c030e 142399e
Author: Dosite Iradukunda Cyiza <145858744+dosite-cyiza@users.noreply.github.com>
Date:   Sun Jul 20 14:16:24 2025 +0200

    Merge pull request #14 from dosite-cyiza/ft/service-redesign

    ft/service-redesign

commit 142399ef42c466742e7a7564ff6e5fd4596b1db7 (origin/ft/service-redesign, ft/service-redesign)
Merge: 3db4be5 a8c030e
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sun Jul 20 14:13:27 2025 +0200

    Merge branch 'main' into ft/service-redesign

commit a8c030e2fe5fdec75416778f6203cdb9844b04a9
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sun Jul 20 14:10:23 2025 +0200

    new changes in services page

commit 49e0c03547f17d5e61b2b1d0e5316ceec7e5945a
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sun Jul 20 14:07:22 2025 +0200

    new changes in services page

commit 3db4be5301ba8caef1e3f17d8e3cc34e60bdf138
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sun Jul 20 14:02:38 2025 +0200

    ft/service-redesign

commit 9022fc3d708a9cc98089e08e189e7e5d60de8dd5
Merge: de20c5f 47179ac
Author: Dosite Iradukunda Cyiza <145858744+dosite-cyiza@users.noreply.github.com>
Date:   Sat Jul 19 19:55:20 2025 +0200

    Merge pull request #13 from dosite-cyiza/ft/bundle-2

    Bundle 2 Exercise 1

commit 47179ac28a57051c7b333cd9aa2a176baeacb29c (origin/ft/bundle-2, ft/bundle-2)
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sat Jul 19 19:53:53 2025 +0200

    Bundle 2 Exercise 1

commit de20c5ff821502d71f0130d6123b26f6cae1603f
Merge: e6ccefd 072574b
Author: Dosite Iradukunda Cyiza <145858744+dosite-cyiza@users.noreply.github.com>
Date:   Sat Jul 19 19:51:20 2025 +0200

    Merge pull request #12 from dosite-cyiza/ft/bundle-2

    Bundle 2 Exercise 1

commit 072574b832d0d6ee31655dcb1bc9ac8758f481b8
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sat Jul 19 19:48:49 2025 +0200

    Bundle 2 Exercise 1

commit e6ccefd655e2778e5d7fc7bbacb89c14778f4f28
Merge: d5d3063 40f5967
Author: Dosite Iradukunda Cyiza <145858744+dosite-cyiza@users.noreply.github.com>
Date:   Sat Jul 19 19:46:46 2025 +0200

    Merge pull request #11 from dosite-cyiza/ft/bundle-2

    feat: services.html

commit 40f5967f4e9e7a2de6670d53f380f324b4f510c6
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sat Jul 19 19:42:18 2025 +0200

    feat: services.html

commit d5d306314f957c6e4ecd6f2ff14c5808a8a22df3
Merge: e85931b 2cd314a
Author: Dosite Iradukunda Cyiza <145858744+dosite-cyiza@users.noreply.github.com>
Date:   Sat Jul 19 19:35:48 2025 +0200

    Merge pull request #10 from dosite-cyiza/dev

    Bundle 1 Exercise 2

commit 2cd314a1349757f8cde254861919d9fd7501a6e7 (origin/dev, dev)
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sat Jul 19 19:33:07 2025 +0200

    Bundle 1 Exercise 2

commit 5dc96d824ee5bbf646aee9c537ef0f0995687c2c
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sat Jul 19 19:24:35 2025 +0200

    setup project

commit e85931b7db8f3a5f44ad99008145dee0e00a89db
Merge: 55e0a8c 383bc5a
Author: Dosite Iradukunda Cyiza <145858744+dosite-cyiza@users.noreply.github.com>
Date:   Sat Jul 19 19:09:38 2025 +0200

    Merge pull request #9 from dosite-cyiza/dev

    Bundle1 Exercise 1

commit 383bc5a666bd2d41f4b1e3c91264bf0161ee5ea1
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sat Jul 19 19:08:50 2025 +0200

    Bundle1 Exercise 1

commit 55e0a8c99d4a5a3148727324a4043586cb320e0d (test)
Merge: 0f046d0 8c91da7
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sat Jul 19 18:58:29 2025 +0200

    Merge branch 'main' of https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions

commit 0f046d0aca3eaf46fe54096c0aa64571501b603a
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sat Jul 19 18:54:18 2025 +0200

    initial commit

commit 8fe41212521f711950bd06634d05df58a7e54869
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sat Jul 19 18:50:36 2025 +0200

    initial commit

commit 8c91da71c66aea8aa3e21076c5031b4475799a50
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sat Jul 19 18:34:47 2025 +0200

    remove all files

commit 68c54a7c0ec80042a01bc1e79863e0e51855baa9
Merge: bdda67d cab0620
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 19:04:20 2025 +0200

    Merge branch 'main' of https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions

commit bdda67d1efce817cee966cf06d4299653dae03d4
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 19:02:48 2025 +0200

    Bundle 2 Exercise 2

commit cab0620a2a8b0c03119bc681b1e76da5adc19c01
Merge: 05b64e5 775a9a0
Author: Dosite Iradukunda Cyiza <145858744+dosite-cyiza@users.noreply.github.com>
Date:   Thu Jul 17 18:58:27 2025 +0200

    Merge pull request #3 from dosite-cyiza/ft/service-redesign

    New File service.html

commit 775a9a095176954eb8ac12ecb0ce8de70f66128b
Merge: a880587 05b64e5
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 18:47:23 2025 +0200

    new changes in services.html

commit 05b64e5ad8913e1107fc9f32a87940a2065e45d5
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 18:23:37 2025 +0200

    adding new changes in services html

commit a880587b9e3899533ec5b2c1e4f8d31b858b1a95
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 18:20:30 2025 +0200

    new changes in file

commit 249a54f7b633d89fe27e2c91fc88cbce78c570e7
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 18:17:38 2025 +0200

    New File service.html

commit c856ff32b5642e3a38e447a094613ce806b2e022
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 18:02:33 2025 +0200

    bundle 2 Exercise 1 Terminal history

commit c48af74283d04186b9ab324664e92cad936ab8e7
Merge: 8882c8c f2b24d1
Author: Dosite Iradukunda Cyiza <145858744+dosite-cyiza@users.noreply.github.com>
Date:   Thu Jul 17 17:50:06 2025 +0200

    Merge pull request #1 from dosite-cyiza/ft/bundle-2

    Ft/bundle 2

commit 8882c8c6bb70cbe745cdcfb69fdf3659a016b46b
Merge: 1dff6d7 5b2770b
Author: Dosite Iradukunda Cyiza <145858744+dosite-cyiza@users.noreply.github.com>
Date:   Thu Jul 17 16:40:55 2025 +0200

    Merge pull request #2 from dosite-cyiza/dev

    Adding Bundle1- Exercise 2

commit 5b2770bdfb50f795024ceb91468aeb41aef2e6f8
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 16:36:54 2025 +0200

    terminal history ##bunde 1 exercise 1

commit f2b24d113cc8d81337222bd02debfdf67e764ddb
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 15:45:11 2025 +0200

    setup services page

commit 57f9484a719ca4f28ebf6043893158cb6b643126
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 15:17:58 2025 +0200

    setup home and about pages

commit 89bff22d1bf557665336722c165ddc62ddb3d0f3
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 13:01:26 2025 +0200

    setup

commit fad816e7815c11147eba477140cde57cabe3e787
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 12:19:55 2025 +0200

    Bunde1 Exercise 1

commit 1dff6d726a9d7e624b9eee20cbdf65eebcffd5c6
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

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/team-page)
$ git cherry-pick 88587bb0fb1fcd95d7c1d746d942f2e28c0afbae
On branch ft/team-page
You are currently cherry-picking commit 88587bb.
  (all conflicts fixed: run "git cherry-pick --continue")
  (use "git cherry-pick --skip" to skip this patch)
  (use "git cherry-pick --abort" to cancel the cherry-pick operation)

nothing to commit, working tree clean
The previous cherry-pick is now empty, possibly due to conflict resolution.
If you wish to commit it anyway, use:

    git commit --allow-empty

Otherwise, please use 'git cherry-pick --skip'

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/team-page|CHERRY-PICKING)
$ git cherry-pick --skip

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/contact-page)
$ git cherry-pick 88587bb0fb1fcd95d7c1d746d942f2e28c0afbae
CONFLICT (modify/delete): team.html deleted in HEAD and modified in 88587bb (feat: team page).  Version 88587bb (feat: team page) of team.html left in tree.
error: could not apply 88587bb... feat: team page
hint: After resolving the conflicts, mark them with
hint: "git add/rm <pathspec>", then run
hint: "git cherry-pick --continue".
hint: You can instead skip this commit with "git cherry-pick --skip".
hint: To abort and get back to the state before "git cherry-pick",
hint: run "git cherry-pick --abort".
hint: Disable this message with "git config set advice.mergeConflict false"

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/contact-page|CHERRY-PICKING)
$ git add team.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/contact-page|CHERRY-PICKING)
$ git cherry-pick --continue
[ft/contact-page 4c6720b] feat: team page
 Date: Sun Jul 20 17:38:12 2025 +0200
 1 file changed, 11 insertions(+)
 create mode 100644 team.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/contact-page)
$ git add contact.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/contact-page)
$ git commit -m"New changes in contact page"
On branch ft/contact-page
nothing to commit, working tree clean

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/contact-page)
$ git add contact.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/contact-page)
$ git commit -m"New change in contact page"
[ft/contact-page 6425577] New change in contact page
 1 file changed, 4 insertions(+)

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/contact-page)
$ git push origin ft/contact-page
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 16 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 671 bytes | 671.00 KiB/s, done.
Total 6 (delta 4), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (4/4), completed with 2 local objects.
To https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions.git
   253ffbc..6425577  ft/contact-page -> ft/contact-page

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/contact-page)
$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/faq-page)
$ touch faq.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/faq-page)
$ git add faq.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/faq-page)
$ git commit -m"feat: Faq page"
[ft/faq-page 813bbc8] feat: Faq page
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 faq.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/faq-page)
$ git push origin ft/faq-page
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 16 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 242 bytes | 242.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions/pull/new/ft/faq-page
remote:
To https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions.git
 * [new branch]      ft/faq-page -> ft/faq-page

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/faq-page)
$ git log
commit 813bbc8573252c717fe606f2b9b6b4b598bb9898 (HEAD -> ft/faq-page, origin/ft/faq-page)
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sun Jul 20 17:59:21 2025 +0200

    feat: Faq page

commit 6425577474d9bcee8752cbbe156c5955e44dbb9b (origin/ft/contact-page, ft/contact-page)
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sun Jul 20 17:54:45 2025 +0200

    New change in contact page

commit 4c6720b5eed6d191244148229b2291fd73cd93e6
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sun Jul 20 17:38:12 2025 +0200

    feat: team page

commit 253ffbceba739c0d188306876186f366ea1a337a
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sun Jul 20 17:42:34 2025 +0200

    feat: contact page

commit 61c7b53c2ea85263d4a5c113962ee90e41a7f941
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sun Jul 20 17:41:33 2025 +0200

    feat: contact page

commit df76fa9997c6de6ce3bd50dc7769aae34e6eb33f (origin/main, main)
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sun Jul 20 14:24:20 2025 +0200

    Bundle 2 Exercise 2

commit def696f8e637e34fe33517e93f3f48be90503ba9
Merge: a8c030e 142399e
Author: Dosite Iradukunda Cyiza <145858744+dosite-cyiza@users.noreply.github.com>
Date:   Sun Jul 20 14:16:24 2025 +0200

    Merge pull request #14 from dosite-cyiza/ft/service-redesign

    ft/service-redesign

commit 142399ef42c466742e7a7564ff6e5fd4596b1db7 (origin/ft/service-redesign, ft/service-redesign)
Merge: 3db4be5 a8c030e
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sun Jul 20 14:13:27 2025 +0200

    Merge branch 'main' into ft/service-redesign

commit a8c030e2fe5fdec75416778f6203cdb9844b04a9
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sun Jul 20 14:10:23 2025 +0200

    new changes in services page

commit 49e0c03547f17d5e61b2b1d0e5316ceec7e5945a
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sun Jul 20 14:07:22 2025 +0200

    new changes in services page

commit 3db4be5301ba8caef1e3f17d8e3cc34e60bdf138
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sun Jul 20 14:02:38 2025 +0200

    ft/service-redesign

commit 9022fc3d708a9cc98089e08e189e7e5d60de8dd5
Merge: de20c5f 47179ac
Author: Dosite Iradukunda Cyiza <145858744+dosite-cyiza@users.noreply.github.com>
Date:   Sat Jul 19 19:55:20 2025 +0200

    Merge pull request #13 from dosite-cyiza/ft/bundle-2

    Bundle 2 Exercise 1

commit 47179ac28a57051c7b333cd9aa2a176baeacb29c (origin/ft/bundle-2, ft/bundle-2)
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sat Jul 19 19:53:53 2025 +0200

    Bundle 2 Exercise 1

commit de20c5ff821502d71f0130d6123b26f6cae1603f
Merge: e6ccefd 072574b
Author: Dosite Iradukunda Cyiza <145858744+dosite-cyiza@users.noreply.github.com>
Date:   Sat Jul 19 19:51:20 2025 +0200

    Merge pull request #12 from dosite-cyiza/ft/bundle-2

    Bundle 2 Exercise 1

commit 072574b832d0d6ee31655dcb1bc9ac8758f481b8
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sat Jul 19 19:48:49 2025 +0200

    Bundle 2 Exercise 1

commit e6ccefd655e2778e5d7fc7bbacb89c14778f4f28
Merge: d5d3063 40f5967
Author: Dosite Iradukunda Cyiza <145858744+dosite-cyiza@users.noreply.github.com>
Date:   Sat Jul 19 19:46:46 2025 +0200

    Merge pull request #11 from dosite-cyiza/ft/bundle-2

    feat: services.html

commit 40f5967f4e9e7a2de6670d53f380f324b4f510c6
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sat Jul 19 19:42:18 2025 +0200

    feat: services.html

commit d5d306314f957c6e4ecd6f2ff14c5808a8a22df3
Merge: e85931b 2cd314a
Author: Dosite Iradukunda Cyiza <145858744+dosite-cyiza@users.noreply.github.com>
Date:   Sat Jul 19 19:35:48 2025 +0200

    Merge pull request #10 from dosite-cyiza/dev

    Bundle 1 Exercise 2

commit 2cd314a1349757f8cde254861919d9fd7501a6e7 (origin/dev, dev)
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sat Jul 19 19:33:07 2025 +0200

    Bundle 1 Exercise 2

commit 5dc96d824ee5bbf646aee9c537ef0f0995687c2c
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sat Jul 19 19:24:35 2025 +0200

    setup project

commit e85931b7db8f3a5f44ad99008145dee0e00a89db
Merge: 55e0a8c 383bc5a
Author: Dosite Iradukunda Cyiza <145858744+dosite-cyiza@users.noreply.github.com>
Date:   Sat Jul 19 19:09:38 2025 +0200

    Merge pull request #9 from dosite-cyiza/dev

    Bundle1 Exercise 1

commit 383bc5a666bd2d41f4b1e3c91264bf0161ee5ea1
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sat Jul 19 19:08:50 2025 +0200

    Bundle1 Exercise 1

commit 55e0a8c99d4a5a3148727324a4043586cb320e0d (test)
Merge: 0f046d0 8c91da7
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sat Jul 19 18:58:29 2025 +0200

    Merge branch 'main' of https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions

commit 0f046d0aca3eaf46fe54096c0aa64571501b603a
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sat Jul 19 18:54:18 2025 +0200

    initial commit

commit 8fe41212521f711950bd06634d05df58a7e54869
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sat Jul 19 18:50:36 2025 +0200

    initial commit

commit 8c91da71c66aea8aa3e21076c5031b4475799a50
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Sat Jul 19 18:34:47 2025 +0200

    remove all files

commit 68c54a7c0ec80042a01bc1e79863e0e51855baa9
Merge: bdda67d cab0620
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 19:04:20 2025 +0200

    Merge branch 'main' of https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions

commit bdda67d1efce817cee966cf06d4299653dae03d4
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 19:02:48 2025 +0200

    Bundle 2 Exercise 2

commit cab0620a2a8b0c03119bc681b1e76da5adc19c01
Merge: 05b64e5 775a9a0
Author: Dosite Iradukunda Cyiza <145858744+dosite-cyiza@users.noreply.github.com>
Date:   Thu Jul 17 18:58:27 2025 +0200

    Merge pull request #3 from dosite-cyiza/ft/service-redesign

    New File service.html

commit 775a9a095176954eb8ac12ecb0ce8de70f66128b
Merge: a880587 05b64e5
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 18:47:23 2025 +0200

    new changes in services.html

commit 05b64e5ad8913e1107fc9f32a87940a2065e45d5
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 18:23:37 2025 +0200

    adding new changes in services html

commit a880587b9e3899533ec5b2c1e4f8d31b858b1a95
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 18:20:30 2025 +0200

    new changes in file

commit 249a54f7b633d89fe27e2c91fc88cbce78c570e7
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 18:17:38 2025 +0200

    New File service.html

commit c856ff32b5642e3a38e447a094613ce806b2e022
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 18:02:33 2025 +0200

    bundle 2 Exercise 1 Terminal history

commit c48af74283d04186b9ab324664e92cad936ab8e7
Merge: 8882c8c f2b24d1
Author: Dosite Iradukunda Cyiza <145858744+dosite-cyiza@users.noreply.github.com>
Date:   Thu Jul 17 17:50:06 2025 +0200

    Merge pull request #1 from dosite-cyiza/ft/bundle-2

    Ft/bundle 2

commit 8882c8c6bb70cbe745cdcfb69fdf3659a016b46b
Merge: 1dff6d7 5b2770b
Author: Dosite Iradukunda Cyiza <145858744+dosite-cyiza@users.noreply.github.com>
Date:   Thu Jul 17 16:40:55 2025 +0200

    Merge pull request #2 from dosite-cyiza/dev

    Adding Bundle1- Exercise 2

commit 5b2770bdfb50f795024ceb91468aeb41aef2e6f8
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 16:36:54 2025 +0200

    terminal history ##bunde 1 exercise 1

commit f2b24d113cc8d81337222bd02debfdf67e764ddb
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 15:45:11 2025 +0200

    setup services page

commit 57f9484a719ca4f28ebf6043893158cb6b643126
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 15:17:58 2025 +0200

    setup home and about pages

commit 89bff22d1bf557665336722c165ddc62ddb3d0f3
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 13:01:26 2025 +0200

    setup

commit fad816e7815c11147eba477140cde57cabe3e787
Author: dosite-cyiza <dositecyiza@gmail.com>
Date:   Thu Jul 17 12:19:55 2025 +0200

    Bunde1 Exercise 1

commit 1dff6d726a9d7e624b9eee20cbdf65eebcffd5c6
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

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/faq-page)
$ git add faq.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/faq-page)
$ git commit -m"feat: faq page"
[ft/faq-page a67cf80] feat: faq page
 1 file changed, 11 insertions(+)

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/faq-page)
$ git push origin ft/faq-page
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 413 bytes | 413.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions.git
   813bbc8..a67cf80  ft/faq-page -> ft/faq-page

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/faq-page)
$ git revert 4c6720b5eed6d191244148229b2291fd73cd93e6
[ft/faq-page 907b9c5] Revert "feat: team page"
 1 file changed, 11 deletions(-)
 delete mode 100644 team.html

user@Dosite-Cyiza-Laptop MINGW64 /e/Exercises/Exercises/Gym-Git-Exercises-Solutions (ft/faq-page)
$ git push origin ft/faq-page
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 16 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 272 bytes | 272.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/dosite-cyiza/Gym-Git-Exercises-Solutions.git
   a67cf80..907b9c5  ft/faq-page -> ft/faq-page

```