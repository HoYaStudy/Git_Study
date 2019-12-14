# Diff

어떤 내용이 변경되었는지 보여주는 명령어이다.

Modified 이지만, staged 상태가 아닌 file의 내용을 비교한다. 즉, working directory와 staging area의 file 내용을 비교한다.

---

#### `$ git diff <commit 1> <commit 2>`

변경된 내용을 보여준다.

---

#### `$ git diff --cached <commit 1> <commit 2>`
#### `$ git diff --staged <commit 1> <commit 2>`

* `--cached` : **.git repository**와 **staging area**의 file 내용을 비교한다.
* `--staged` : `--cached`와 동일하다.

---

#### `$ git diff <commit 1> <commit 2>`
#### `$ git diff <commit 1>..<commit 2>`

1번을 기준으로 2개의 차이를 비교한다.

하나를 생략하면 `HEAD`를 사용하는 것으로 가정한다.

---

#### `$ git diff <commit 1>...<commit 2>`

Show the diff of what is in \<commit 2> that is not in \<commit 1>.

두 개의 공통 조상으로부터 2번 까지의 차이점을 모두 비교한다.

하나를 생략하면 `HEAD`를 사용하는 것으로 가정한다.

---
