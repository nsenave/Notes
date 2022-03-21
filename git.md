# Git

### Local / global settings

https://stackoverflow.com/questions/42167345/git-set-local-user-name-and-user-email-different-for-each-repo

### Remove local branches that are not in remote

https://gist.github.com/RomuloOliveira/71aceda5cb946f5ffdf7

```shell
git branch -vvv | grep gone | grep -v master | cut -f 3 -d " " # | xargs git branch -D
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
