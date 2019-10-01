# Checkout

Branch를 변경하고 working directory의 file을 교체하는 명령어이다.

---

#### `$ git checkout <branch>`

HEAD pointer가 명시한 branch를 가리킨다.

---

#### `git checkout <commit>`

특정 commit을 checkout하고, detached HEAD 상태가 된다.

---

#### `$ git checkout HEAD <filename>`

Working directory에서 변경된 부분을 버린다.

---

#### `$ git checkout -b <branch>`
#### `$ git checkout -B <branch>`

-b option을 추가하면 branch 명령어도 수행한다. 즉, branch 명령어 처리 후 checkout 명령어를 처리한다.
-B option을 추가하면, 이미 branch가 존재할 경우 reset을 한다. `git branch -f` 명령과 같다.

#### `$ git checkout -b <new_branch> <branch_parent>`

parent branch로부터 새 branch를 생성한다.

#### `$ git checkout -b <local_branch_name> <remote_name/remote_branch_name>`

원격 저장소의 branch에서 시작하는 local branch를 만든다.

#### `$ git checkout -b <branch> <tag>`

Tag가 가리키는 commit을 기반으로 branch를 만들고, HEAD pointer가 가리키게 한다.

---

#### `$ git checkout -t <remote/branch>`
#### `$ git checkout --track <remote/branch>`

-t (--track) option을 추가하면 local 저장소에 branch를 자동으로 생성한 후, remote branch를 tracking 한다.

---

#### `$ git checkout -- <filename>`

-- option을 추가하면 수정됐지만 commit되지 않은 file을 복구한다.

---

|                            | HEAD | Index | Workdir | WD Safe? |
| -------------------------- | ---- | ----- | ------- | -------- |
| **Commit Level**           |      |       |         |          |
| `reset --soft [commit]`    | REF  | NO    | NO      | YES      |
| `reset [commit]`           | REF  | YES   | NO      | YES      |
| `reset --hard [commit]`    | REF  | YES   | YES     | **NO**   |
| `checkout [commit]`        | HEAD | YES   | YES     | YES      |
| **File Level**             |      |       |         |          |
| `reset (commit) [file]`    | NO   | YES   | NO      | YES      |
| `checkout (commit) [file]` | NO   | YES   | YES     | **NO**   |
