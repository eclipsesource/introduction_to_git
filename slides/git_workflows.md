.left-column[
## What is Git
## Git basics
## Advanced
## Oh Shit!
## GitHub
## Workflows
]

.right-column[
GitHub supports several different workflows. We already discussed the
*Fork and Pull* model with separate repositories. You can also work in
a **shared repository model** where everyone shares a single repository.

In this model, you should create **feature branches** for each feature you are
working on. Iterate on the feature (either collaboratively or on your own),
and when you are satisfied with the feature, issue a *pull request*.

**Tip:** Anything in `master` should always be deployable!

**Tip:** Pull requests are just the beginning. Use the pull request to discuss /
review the code and improve it.

**Tip:** Test everything in master. If changes cause problems, **revert** them.

]
---

.left-column[
## What is Git
## Git basics
## Advanced
## Oh Shit!
## GitHub
## Workflows
### C.I.
]

.right-column[
*Continuous Integration (CI) is a development practice that requires developers
to integrate code into a shared repository several times a day.*

Each commit (or at least each push) to a feature branch should trigger a build.
* Does the code compile
* Do the tests pass
* Do the *linters* (code style checker) produce any warnings

If any of these fail, disallow any merging / pull requests!

This gives you great confidence that you are not introducing any regressions
and that `master` is always deployable. However, this only works if you
write tests!

Checkout [https://travis-ci.org/](https://travis-ci.org/) a free Continuous
Integration service that can be integrated with GitHub.

]
