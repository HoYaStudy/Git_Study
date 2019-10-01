# Renaming Git Branch

```sh
$ git checkout <old_branch>
$ git branch -m <new_branch>
$ git push origin --delete <old_branch>
$ git push origin -u <new_branch>
```
