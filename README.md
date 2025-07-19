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