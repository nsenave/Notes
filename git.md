# Git

### Local / global settings

https://stackoverflow.com/questions/42167345/git-set-local-user-name-and-user-email-different-for-each-repo

### Remove local branches that are not in remote

https://gist.github.com/RomuloOliveira/71aceda5cb946f5ffdf7

```shell
git branch -vvv | grep gone | grep -v master | cut -f 3 -d " " # | xargs git branch -D
```

### Find local branches that has no remote

https://stackoverflow.com/questions/15661853/list-all-local-branches-without-a-remote

https://stackoverflow.com/a/31776247/13425151

```shell
git branch --format "%(refname:short) %(upstream)"
git branch --format "%(refname:short) %(upstream)" | awk '{if (!$2) print $1;}'
```

### Remove tags that no longer are in remote

https://stackoverflow.com/questions/1841341/remove-local-git-tags-that-are-no-longer-on-the-remote-repository

https://stackoverflow.com/a/54297675/13425151

```shell
git fetch --prune --prune-tags
```

### Clone specific branch

https://stackoverflow.com/questions/1911109/how-do-i-clone-a-specific-git-branch

```shell
git clone --single-branch --branch <branchname> <remote-repo>
```

### Remove last pushed commit

https://stackoverflow.com/questions/448919/how-can-i-remove-a-commit-on-github

```shell
git reset --soft HEAD^
git push origin +branchName --force
```

```shell
git push -f origin HEAD^:master
```

### Set the editor

https://stackoverflow.com/questions/52195877/how-can-i-fix-git-commit-error-waiting-for-your-editor-to-close-the-file-wi

```shell
git config --global core.editor "'C:\Users\user\AppData\Local\Programs\Microsoft VS Code\Code.exe' -n -w"
```

### Change the author of commit

https://stackoverflow.com/questions/3042437/how-to-change-the-commit-author-for-a-single-commit

### On commit granularity

- https://kennyballou.com/blog/2021/03/commit-granularity/index.html#org241ce3d
- https://gitforteams.com/resources/commit-granularity.html
