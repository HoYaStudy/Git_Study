# Clean

작업중이던 file들을 삭제하는 명령어이다.

---

#### `$ git clean -d -n -x`

Working directory안의 untracked file들을 모두 삭제한다.

-d option을 추가하면 하위 directory까지 적용한다.

-n option을 추가하면 삭제될 file을 보여준다.

-x option을 추가하면 .gitignore에 명시된 file도 삭제한다.

---

#### `$ git clean -i`

-i option을 추가하면 대화형으로 삭제한다.

---
