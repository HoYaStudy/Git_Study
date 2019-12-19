# Difftool

Diff tool을 사용하여 revision 간의 비교와 편집을 할 수 있도록 하는 명령어이다.

Diff 명령어와 동일한 option과 argument를 허용한다.

---

#### `$ git difftool <commit 1> <commit 2>`

Diff tool을 사용하여 차이점을 보여준다.

---

#### `$ git difftool -d <commit 1> <commit 2>`
#### `$ git difftool --dir-diff <commit 1> <commit 2>`

수정된 file을 임시 위치에 복사하고 그것을 사용하여 directory 비교를 한다.

---
