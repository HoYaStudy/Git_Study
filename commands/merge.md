# Merge

commit을 합치는 명령어이다.

* Merge할 branch가 가리키는 commit이 현재 branch의 commit의 upstream branch라면 단순히 pointer만 이동시키는 Fast-forward merge를 한다.
* 현재 branch와 merge할 branch가 직접적인 조상관계가 아니라면 각 branch가 가리키는 commit 2개와 최적의 공통 조상 commit 하나를 이용하여 3-way merge를 한다.

---

#### `$ git merge <branch>`

현재 branch에 명시한 branch를 합친다.

---

#### `$ git merge --abort`

--abort option을 추가하면 충돌이 발생했을 경우, merge하기 전으로 되돌린다.

---

#### `$ git merge -X <option>`
#### `$ git merge --strategy=<strategy>`

#### `$ git merge -Xignore-all-space <branch>`

-Xignore-all-space option을 추가하면 모든 공백을 무시한다.

#### `$ git merge -Xignore-space-change <branch>`

-Xignore-space-change option을 추가하면 연속된 공백을 1개로 취급한다.

---

#### `$ git mergetool`

merge.tool 설정에 있는 merge tool을 실행한다.

---
