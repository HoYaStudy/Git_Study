# Branch

작업 공간을 분리하여 독립적인 작업 공간을 만들어주는 명령어이다.

---

#### `$ git branch`

Branch 목록을 보여준다. `*` 표시가 붙은 branch가 현재 checkout되어 작업중인 branch이다.

---

#### `$ git branch <branch>`

해당 이름의 branch를 만든다.

---

#### `$ git branch --list`

--list option을 추가하면 모든 local branch를 보여준다.

---

#### `$ git branch -r`
#### `$ git branch --remotes`

-r option을 추가하면 모든 remote branch를 보여준다.

---

#### `$ git branch -a`
#### `$ git branch --all`

-a option을 추가하면 모든 local, remote branch를 보여준다.

---

#### `$ git branch --contains <commit>`

--contains option을 추가하면 해당 commit 객체를 포함하는 모든 branch 목록을 보여준다.

---

#### `$ git branch -v`
#### `$ git branch -vv`
#### `$ git branch --verbose`

-v option을 추가하면 branch별 commit message도 함께 보여준다.

--vv options을 추가하면 tracking branch 설정도 함께 보여준다. 단, fetch 시점의 data를 기준으로 한다.

> Ex) $ git fetch --all && git branch -vv

최신 data를 기준으로 `$ git branch -vv` 명령을 실행한다.

---

#### `$ git branch --merged`

--merged option을 추가하면 merge된 branch를 보여준다.

---

#### `$ git branch --no-merged`

--no-merged option을 추가하면 아직 merge되지 않은 branch를 보여준다. -d option으로 삭제되지 않는다.

---

#### `$ git branch -d <branch>`
#### `$ git branch --delete <branch>`

-d option을 추가하면 merge된 branch를 삭제한다.

---

#### `$ git branch -D <branch>`

-D option을 추가하면 merge되지 않은 branch를 강제로 삭제한다.

---

#### `$ git branch -u <remote/branch>`
#### `$ git branch --set-upstream-to <remote/branch>`

-u option을 추가하면 local 저장소에 있는 branch가 remote 저장소의 branch를 tracking 한다.

---
