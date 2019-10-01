# Add

Staging area에 file을 추가하는 명령어이다.

---

#### `$ git add <pathspec>`

Staging area에 명시한 file들을 추가한다.

---

#### `$ git add -A`
#### `$ git add --all`

-A (--all) option을 추가하면 git root directory 하위의 모든 수정사항과 새로운 file을 추가한다.

---

#### `$ git add *`

*를 \<pathspec\>에 사용하면 현재 directory 하위의 모든 수정사항과 새로운 file을 추가한다.

---

#### `$ git add -i`
#### `$ git add --interactive`

-i (--interactive) option을 추가하면 대화형 mode로 추가한다.

---

#### `$ git add -p <pathspec>`
#### `$ git add --patch <pathspec>`

-p (--patch) option을 추가하면 file의 수정사항의 일부만을 대화형 mode로 추가한다. 변경사항 하나를 **hunk** 단위라고 한다.

---
