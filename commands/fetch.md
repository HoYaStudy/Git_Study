# Fetch

Remote 저장소에서 git data를 가져오는 명령어이다.

가져온 내용으로 작업을 하려면 local 저장소에 merge 해야한다.

---

#### `$ git fetch <remote_name>`

Remote 저장소에서 data를 가져온다. 자동으로 merge 하지는 않는다.

---

#### `$ git fetch -p <remote_name>`
#### `$ git fetch --prune <remote_name>`

* `-p` : Fetch하기 전에, remote에 더이상 존재하지 않는 reference들을 삭제한다.

---
