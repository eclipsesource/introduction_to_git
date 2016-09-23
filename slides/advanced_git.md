.left-column[
## What is Git
## Git basics
## Advanced
]

.right-column[
 <img src="images/git-is-hard.png" class="centered" width="300px"/>

.centered-text[[Source](http://merrigrove.blogspot.ca/2014/02/why-heck-is-git-so-hard-places-model-ok.html)
]
* Git is often considered overly complex
* Makes easy things easy and hard things possible?
* Easy is objective
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
<img src="images/reset-workflow.png" class="centered" width="500px"/>
* Work on files in your current working directory
* `git add` adds the file to the index
* `git commit` commits index
* `git reset` can be used to reset where HEAD points

**Reset** is a very powerful command, but make sure you understand what it's
doing! Read [Reset Demystified](https://git-scm.com/book/en/v2/Git-Tools-Reset-Demystified).

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
Every data storing action (commit, reset, pull, etc...) is stored in the
**reflog**. Use `git reflog` to see this log. Use this as your safety net.

<img src="images/reflog.png" width="500px" class="centered"/>

Reflog combined with checkout and reset can be used to surgically fix your
git repository.
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
Add a `.gitignore` file to your repository to intentionally specify files
to ignore. Good candidates are binary files, log files, temporary files, etc...

Checkout [Git Ignore Templates](https://github.com/github/gitignore) for a
collection of `.gitignore` files.
]
