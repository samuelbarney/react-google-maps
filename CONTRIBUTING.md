# Contributor Guideline


## Commit

> One golden rule: follow [the commit format][commit-format]

We use [standard-version][standard-version] to automatically generate [CHANGELOG.md][CHANGELOG.md] from the `git commit` history. Please **do** follow [the commit format][commit-format] before commiting.


## PR

Simple rules:

* Do rebase before merging.
* Do fixup/squash commits when it's necessary.
* **Do NOT** bump package.json version.
* **Do NOT** contains any changes inside `lib` folder. (i.e. you shouldn't run `npm run build` yourself)


### For contributor raised ones

Since contributors have write permission for this repository, you're free to do changes. But in order to keep changes trackable, please follow the guideline here:

> Create a PR with your branch

> In local, merge your branch to `master`. **Make sure** it's a `fast-forward` merge.

> Push your master to `origin` and you should see the PR is automatically closed.

**Examples**: #269, #270, #271


### PR (for contributor raised ones)

* Don't use merge commit (already disabled)
* **Always** use squash merge. Reformat the commit message to match this guideline.
* Include `thanks to @commitAuthor` message
* Include `closes #pr-number, #issue-number` message if applicable

**Examples**: #252, #259


## Release

Right now, only the author has the write permission on npm. But I'll document the procedure here:

* `npm run release`
* Now the changes is automatically committed
* It automatically bumps `package.json` according to the `git commit` history
* [CHANGELOG.md][CHANGELOG.md] is generated for the version as well
* `git tag` for the version is tagged to the commit too
* The last step is release the changes to `origin` and `npm`.


[standard-version]: https://github.com/conventional-changelog/standard-version
[CHANGELOG.md]: ./CHANGELOG.md
[commit-format]: https://github.com/conventional-changelog/standard-version#commit-message-convention-at-a-glance
