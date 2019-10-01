# File의 수정 사항을 제거할 때

```python
if 수정 사항이 commit 되었나?:
  if Log 기록을 유지하고 싶은가?:
    $ revert <commit>
  else:
    if 해당 branch는 공유 중인가?:
      $ revert <commit>
    else:
      if 삭제하고 싶은 수정 사항이 가장 최신 commit에 있는가?:
        if working directory에 저장하고 싶은 수정 사항이 있는가?:
          $ reset <commit>
        else:
          $ reset --hard <commit>
      else:
        $ rebase --interactive <commit>
else:
  if 수정 사항이 staging area에 있는가?:
    if working directory에 저장하고 싶은 수정 사항이 있는가?:
      $ reset <filename>
      $ checkout -- <filename>
    else:
      $ reset --hard
  else:
    $ checkout -- <filename>
```
