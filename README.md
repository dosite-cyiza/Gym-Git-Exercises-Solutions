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