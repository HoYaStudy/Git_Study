# Change User Information in Commits

기존 commit의 `user.name`과 `user.email`을 변경하는 방법이다.

```sh
#!/bin/bash

git filter-branch -f --env-filter '
OLD_EMAIL="hoya128@nextchip.com"
CORRECT_NAME="llHoYall"
CORRECT_EMAIL="hoya128@gmail.com"
if [ "$GIT_COMMITTER_EMAIL" = "$OLD_EMAIL" ]
then
    export GIT_COMMITTER_NAME="$CORRECT_NAME"
    export GIT_COMMITTER_EMAIL="$CORRECT_EMAIL"
fi
if [ "$GIT_AUTHOR_EMAIL" = "$OLD_EMAIL" ]
then
    export GIT_AUTHOR_NAME="$CORRECT_NAME"
    export GIT_AUTHOR_EMAIL="$CORRECT_EMAIL"
fi
' --tag-name-filter cat -- --branches --tags
```
