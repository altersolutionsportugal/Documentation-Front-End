# Git

## Install Git

[Download in this link and follow the wizard install](https://git-scm.com/downloads)

[Follow this official documentation](https://git-scm.com/doc)

### Git Workflow

The principal branchs are `main`, `release`, `develop`, `feature`.
`main` is for production deploy
`release/v*.*.*` is for pre-production deploy
`develop` is for develop deploy
`feature/**` is for develop new features, make PR to develop.

For publish a new release in pre-production, use the follow pattern `release/v1.0.0`.
The pipeline to deploy in pre will trigger all the new bracnchs in release/v*.*.*

Every PR to production need to be approved for 2 another develop

### Git Commit

Install this lib
```shell
npm install git-commit-msg-linter --save-dev
```

All the commits have to be types.
The default types includes **feat**, **fix**, **docs**, **style**, **refactor**, **test**, **chore**, **perf**, **ci**, **build** and **temp**.
The default max-len is 100 which means the commit message cannot be longer than 100 characters. All the settings can be modified in commitlinterrc.json.

![types reference](https://github.com/altersolutionsportugal/Documentation-Front-End/blob/main/images/git1.png)


### Alias Sugestion

Git commit.
```shell
c = !git add --all && git commit -m
```
Git status.
```shell
s = !git status -s
```
Git log.
```shell
l = !git log --pretty=format:'%C(blue)%h%C(red)%d %C(white)%s - %C(cyan)%cn, %C(green)%cr'
```
Git ammend. (This command takes your staging area and uses it for the commit. If you’ve made no changes since your last commit, then your snapshot will look exactly the same, and all you’ll change is your commit message.)
```shell
amend = !git add --all && git commit --ammend --no-edit
```
