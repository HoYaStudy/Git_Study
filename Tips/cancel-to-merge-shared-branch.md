# Cancel to Merge Shared Branch

```python
if merged commit이 있는가?:
  $ revert --mainline N <commit>
	# 일반적으로 N = 1
	# commit은 반드시 merged commit이어야 한다.
else:
  $ branch --contains <commit>
  if commit이 연속적인가?:
    $ revert --no-commit <commit_keep>_<commit_reject>
		$ add <filename>
		$ commit
  else:
    각각의 잘못된 commit마다 반복한다.
```
