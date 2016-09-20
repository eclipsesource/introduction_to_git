.left-column[
## What is Git
## Git basics
## Advanced
]

.right-column[

]

---
.left-column[
## What is Git
## Git basics
## Advanced
### - Stash
]

.right-column[
If you want to switch branches to work on something else, but are not ready
to commit your current work yet, use the `git stash` command.

Stashing takes the dirty state of your working directory – that is, your
modified tracked files and staged changes – and saves it on a stack of
unfinished changes that you can reapply at any time.

Use `git stash pop` to apply the most recent stashed change and then
drop it from your stack.

Use `git stash list` to see the stack of stashes you have.

Use `git stash apply` to apply a specific stash.

]

---
.left-column[
## What is Git
## Git basics
## Advanced
### - Stash
### - Rebase
]

.right-column[
**Rebasing** is an alternative to merging when integrating two branches. Unlike
merging, rebasing takes all the changes that were committed on one branch and
applies them to another.
<img src="images/basic-rebase-2.png" width="500px"/>

Consider change-set C4. Instead of merging C4 and C5, C4 can be reapplied
after C5. This results in a new commit C4'.

<img src="images/basic-rebase-3.png" width="500px"/>
]

---
.left-column[
## What is Git
## Git basics
## Advanced
### - Stash
### - Rebase
]

.right-column[
Often you'll rebase to make sure your commits apply cleanly on a remote branch.

`rebase origin/master`

**Do not rebase commits that exist outside your repository.**

Should I rebase or should I merge:

Rebasing *tells the story of **how** your software was made.* This often
produces more readable commit histories. Merging *tells
the story of exactly **what** happened.* This shows every path that
was taken, and every wrong turn that was made.

]

---
.left-column[
## What is Git
## Git basics
## Advanced
### - Stash
### - Rebase
### - Reset
]

.right-column[

]

---
.left-column[
## What is Git
## Git basics
## Advanced
### - Stash
### - Rebase
### - Reset
### - Reflog
]

.right-column[

]

---
.left-column[
## What is Git
## Git basics
## Advanced
### - Stash
### - Rebase
### - Reset
### - Reflog
### - GitIgnore
]

.right-column[

]
