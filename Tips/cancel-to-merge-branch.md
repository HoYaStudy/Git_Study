# Cancel to Merge Branch

```python
if 잘못된 merge 이후 현재 branch에 commit된 것이 있는가?:
  if 다시 merge할 수 있는 필요한 commit이 다른 branch에 존재하는가?:
    $ reset <last_correct_commit>
    $ merge <branch_with_good_commits>
  else:
    $ checkout <commit_before_bad_merge>
    $ checkout -b <safe_branch>
    $ cherry-picl <commit_to_save>
    $ checkout <branch_to_fix>
    $ reset <last_correct_commit>
    $ merge <branch_with_good_commits>
else:
  if 다른 branch가 삭제된 적이 있는가?:
    if 나중에 merge를 재시도 할 것인가?:
      $ checkout -b <safe_branch>
      $ checkout <branch_to_fix>
      $ reset --merge ORIG_HEAD
    else:
      $ reset --merge ORIG_HEAD
  else:
    $ reset --merge ORIG_HEAD
```
