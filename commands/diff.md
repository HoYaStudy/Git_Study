# Diff

어떤 내용이 변경되었는지 보여주는 명령어이다.

Modified 이지만, staged 상태가 아닌 file의 내용을 비교한다. 즉, working directory와 staging area의 file 내용을 비교한다.

---

#### `$ git diff`

변경된 내용을 보여준다.

---

#### `$ git diff --cached`
#### `$ git diff --staged`

--cached option을 추가하면 .git repository와 staging area의 file 내용을 비교한다.

`--staged`는 `--cached`와 동일하다.

---

#### `$ git diff <branchA>...<branchB>`

Show the diff of what is in branchB that is not in branchA.

---
