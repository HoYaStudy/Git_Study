# Cleaning Ignored Files

이미 git에서 tracked 상태인 file이 ignore list에 있을 때, 다시 ignore를 적용하여 untracked 상태로 만드는 방법이다.

```
$ git rm -r --cached .
$ git add .
$ git commit -m "Clean up ignored files"
```
