# Commit

Staging area에 있는 file들을 .git directory에 snapshot으로 저장하는 명령어이다.

---

#### `$ git commit`

Staging area의 파일을 .git directory로 commit 한다.

---

#### `$ git commit -a`
#### `$ git commit --all`

-a option을 추가하면 tracked file을 자동으로 staging area에 추가하여 commit 한다.

---

#### `$ git commit -m "Commit Message"`
#### `$ git commit --message= "Commit Message"`

-m option을 추가하면 commit message를 간략하게 적을 수 있다.

---

#### `$ git commit --amend`

--amend option을 추가하면 마지막 commit message를 수정할 수 있다.

add나 rm 명령으로 commit의 파일을 수정할 수도 있다.

SHA-1 값이 바뀌며, rebase 같이 이미 push한 commit은 수정하면 안 된다.

---
