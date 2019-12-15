# Revert

Revert some existing commits.

---

#### `$ git revert <commit>`

Create new commit that undoes all of the changes made in \<commit\>, then apply it to the current branch.

---

#### `git revert -m parent-number <commit>`
#### `git revert --mainline parent-number <commit>`

* `-m` : Merged commit을 revert 할 때, 어느 쪽을 mainline으로 할 지 결정한다.

> Ex) $ git revert -m1 \<commit>

Merge를 해온 commit의 내용을 revert 한다.

> Ex) $ git revert -m2 \<commit>

Merge가 된 commit의 내용을 revert 한다.

```
    - B -
   /     \
A - - C - - D
```

위와 같은 상황에서, D가 merged commit이고, 현재 branch가 C였고, B를 merge 해왔다고 하자.

`-m1` option을 사용하면 B가 revert 되고, `-m2` option을 사용하면 C가 revert 된다.

---

#### `$ git revert -n <last_commit_to_keep>..<newest_commit_to_reject>`
#### `$ git revert --no-commit <last_commit_to_keep>..<newest_commit_to_reject>`

* `-n` : 여러 commit을 revert 하고, revert된 commit 하나당 하나의 객체를 생성하는 대신 하나의 revert commit을 생성한다.

---
