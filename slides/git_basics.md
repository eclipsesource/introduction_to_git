
.left-column[
## What is Git
## Git basics
]
.right-column[
Several Git clients available:
* IDE Integration (Eclipse, IntelliJ IDEA, etc...)
* gitk, git-gui
* GitHub for Mac and Windows
* SourceTree
* Command line

We will use the command line to teach the basics.
]

---
.left-column[
## What is Git
## Git basics
### - Commits  
]

.right-column[
  .pull-left[
    ```bash
    $ git init
    $ git add a.text
    $ git commit
    ```
  ]
  .pull-right[
1. Create a Git repository
2. Add file `a.text`
3. Commit the change-set
  ]

Write a detailed commit message:
![Default-aligned image](images/commit-message.png)
Git takes care of the:
 - **Who**: author who committed the change-set
 - **When**: timestamp of the change-set
 - **How**: The code you committed

You **should** document:
 - **What**: What does this change-set do
 - **Why**: Why is this important
]

---

.left-column[
  ## What is Git
  ## Git basics
 ### - Commits  
 ### - Status
]
.right-column[
The main tool you use to determine which files are in which state is the
`git status` command.  The **status** tool tell you:
* The files that have changed
* The files that have been staged (changed, and ready for commit)
* The files that are untracked (not part of the repository)
* The files that have been deleted
]

---

.left-column[
  ## What is Git
  ## Git basics
 ### - Commits  
 ### - Status
 ### - Logs
]
.right-column[
 Some advice on writing good commit messages:  
 [http://chris.beams.io/posts/git-commit/](http://chris.beams.io/posts/git-commit/)

 Commit logs should tell the story of **how** your software was developed.
 ![Center-aligned image](images/git_commit.png)

 Work on commits until they are **perfect**. Don't be afraid to *amend* commits,
 but once they are public, they are immutable. .red[*]

 Use `git log` to see the history of your project. Use the `--graph` argument
 to see the merge paths.

 .footnote[.red[*] Once they are public, and in the master / production branch]
]

---
.left-column[
  ## What is Git
  ## Git basics
 ### - Commits  
 ### - Status
 ### - Logs
 ### - Branches
]
.right-column[
 ![Default-aligned image](images/branch.svg)
 *Branching* is the way to work on different versions of a repository at one time

 By default, your repository will have one branch named `master`.

 When you create a branch off `master`, you're making a copy or a snapshot of
 `master` as it was at that point in time.

 Create a new **feature** branch for each feature you work on.

  ```bash
  $ git branch new-awesome-feature
  ```

  Creates a new branch, but does not check it out. Use
  `git checkout -b <branch_name>` to create and checkout the branch.

  Move between branches with `git checkout`.
]

---
.left-column[
  ## What is Git
  ## Git basics
 ### - Commits  
 ### - Status
 ### - Logs
 ### - Branches
 ### - Merging
]
.right-column[
Merging is Git's way of putting a *forked* history back together again.

![Default-aligned image](images/3way-merge.png)

Once you've finished developing a feature, it's important to be able to get
it back into the main code base.

```bash
$ git merge <branch>
```

Merge the specified branch into the current branch. Git will determine
the merge algorithm.
]

---
.left-column[
  ## What is Git
  ## Git basics
 ### - Commits  
 ### - Status
 ### - Logs
 ### - Branches
 ### - Merging
]
.right-column[
 Two common merging algorithms: **Fast Forward** or **3 Way Merge**.

 **Fast Forward:** Used when there is a linear path from the current branch
 tip to the target branch. Instead of actually merging, Git just integrates
 the histories.

 **3 Way Merge:** Used when two branches have diverged. In this case, a new
 commit is created to tie the two branches together.

 If two commits change similar parts of the same file, Git won't be able to
 figure out which one to use. Git will stop the merge so you can **resolve
 the conflicts** manually.

 * Git will tell you which files have conflicts (and where)
 * Manually resolve the conflicts
 * run `git add <file_with_conflict>` to mark as resolved
 * run `git commit` to generate the merge commit
]
