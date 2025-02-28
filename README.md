# Git-Advanced-Exercises

## Part 1:  Refining Git History (10 Challenges)

### 1: Missing File Fix

```bash
Run git status and git log to assess the current state of your repository.
From the status you will see that you forgot to add test4.md in the last commit.
Challenge: Recover from this error by staging/adding test4.md and amending the commit message with an appropriate description.


# Solution

gymimena@Imenas-iMac Git-Advanced-Exercises % git add test4.md && git commit -m "chore: Create fourth file"
[main 9fe9554] chore: Create fourth file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test4.md
gymimena@Imenas-iMac Git-Advanced-Exercises % git log --oneline 
9fe9554 (HEAD -> main) chore: Create fourth file
7924ee6 chore: Create third and fourth files
be25464 chore: Create another file
328e074 chore: Create initial file


```

### Editing Commit History

```bash
It's crucial to maintain accurate commit messages. Modify the message from "Create another file" to "Create second file".
Challenge: Utilize interactive rebasing (git rebase -i HEAD~2) to edit the commit message and ensure clarity.

# Solution
gymimena@Imenas-iMac Git-Advanced-Exercises % git rebase -i HEAD~3 
[detached HEAD d17c64d] chore: Created second file
 Date: Fri Feb 28 14:43:40 2025 +0200
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test2.md
Successfully rebased and updated refs/heads/main.


```