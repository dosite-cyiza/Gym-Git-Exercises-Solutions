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

