# STash

File 수정 중에 commit하지 않고 다른 branch로 변경할 때 임시로 저장하게 해주는 명령어이다. Stash는 modified 상태이면서 tracked 상태인 file과 staging area에 있는 file들을 보관하는 장소이다.

---

#### `$ git stash`

새로운 stash를 만들어 working directory에서 수정한 file들만 저장한다.

---

#### `$ git stash list`

저장한 stash를 보여준다.

---

#### `$ git stash [push]`

Local 수정 사항을 새로운 stash에 저장하고, working tree와 index의 내용을 HEAD로 되돌린다.

---

#### `$ git stash -m <message>`
#### `$ git stash --message <message>`

-m option을 추가하면 stash에 push할 때 message를 추가한다.

---

#### `$ git stash --keep-index`

--keep-index option을 추가하면 staging area에 있는 file은 stash에 저장하지 않는다.

---

#### `$ git stash -u`
#### `$ git stash --include-untracked`

-u option을 추가하면 untracked file도 stash에 저장한다..

---

#### `$ git stash -p`
#### `$ git stash --patch`

-p option을 추가하면 대화형으로 저장할 file을 선택할 수 있다.

---

#### `$ git stash pop`

Stash에 가장 최근에 저장한 file을 불러온 후, stash를 제거한다.

---

#### `$ git stash apply`

Stash에 가장 최근에 저장한 file을 불러온다.

---

#### `$ git stash apply <stash>`

명시한 stash에 저장한 file을 불러온다.

> Ex) $ git stash apply stash@{2}

---

#### `$ git stash apply --index`

--index option을 추가하면 staged 상태였던 file을 staged로 만들어 준다.

---

#### `$ git stash drop <stash>`

명시한 stash를 제거한다.

> Ex) $ git stash drop stash@{0}

---

#### `$ git stash branch <branch>`

명시한 이름으로 branch를 새로 만들어 stash에 저장된 file을 불러온다.

---
