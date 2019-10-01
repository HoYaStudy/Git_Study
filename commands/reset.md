# Reset

Commit을 해제하는 명령어이다.

---

#### `$ git reset <commit>`

Commit을 해제한다. 즉, INDEX를 현재 HEAD가 가리키는 snapshot으로 update한다.

> Ex) $ git reset HEAD^

---

#### `$ git reset <file>`

HEAD에서 file을 INDEX로 옮긴다.

> Ex) $ git reset --mixed HEAD \<file\>

---

#### `$ git reset HEAD <file>`

Staging area의 file을 staging area에서 삭제해 file의 수정사항이 다음 commit에 저장되지 않도록 한다.

---

#### `$ git reset <commit> <file>`

Commit에서 INDEX로 file을 옮긴다.

---

#### `$ git reset --soft <commit>`

--soft option을 추가하면 HEAD가 가리키는 commit만 바꾼다.

> Ex) $ git reset --soft HEAD~

---

#### `$ git reset --mixed <commit>`

Default option이다. --mixed option을 추가하면 INDEX는 바꾸고, working directory는 그대로 둔다.

---

#### `$ git reset --hard <commit>`

--hard option을 추가하면 working directory까지 update한다.

> Ex) $ git reset --hard HEAD~

---

#### `$ git reset --merge ORIG_HEAD`

--merge option을 추가하면 최신 merge를 통해 적용된 모든 commit을 현재 branch에서 삭제한다.

* `ORIG_HEAD` : Reset을 이용해 HEAD를 변경하면, 이전의 HEAD는 .git/ORIG_HEAD라는 이름으로 저장이 된다.

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
