# Cherry-Pick

Apply the changes introduced by some existing commits.

---

#### `$ git cherry-pick <commit>`

하나의 branch commit을 다른 branch로 복사한다.

---

#### `$ git cherry-pick <commit 1>..<commit 2>`

\<commit 1>부터 \<commit 2>까지의 모든 commit을 \<commit1>을 제외하고 가져온다.

---

#### `$ git cherry-pick <commit 1>^..<commit 2>`

\<commit 1>부터 \<commit 2>까지의 모든 commit을 가져온다.

---

#### `$ git cherry-pick -m <parent-number> <commit>`
#### `$ git cherry-pick --mainline <parent-number> <commit>`

* `-m` : Merged commit을 cherry-pick 할 때, 어느 쪽을 mainline으로 할 지 결정한다.

> Ex) $ git revert -m1 \<commit>

Merge를 해온 commit의 내용을 cherry-pick 한다.

> Ex) $ git revert -m2 \<commit>

Merge가 된 commit의 내용을 cherry-pick 한다.

```
    - B -
   /     \
A --- C --- D
```

위와 같은 상황에서, D가 merged commit이고, 현재 branch가 C였고, B를 merge 해왔다고 하자.

`-m1` option을 사용하면 B가 cherry-pick 되고, `-m2` option을 사용하면 C가 cherry-pick 된다.

---
