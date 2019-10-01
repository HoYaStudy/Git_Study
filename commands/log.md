# Log

Commit log를 보는 명령어이다.

---

#### `$ git log`

Log를 보여준다.

#### `$ git log <branchA>..<branchB>`
#### `$ git log ^<branchA> <branchB>`
#### `$ git log <branchB> --not <branchA>`

branchB의 commit 중 branchA에 merge하지 않은 것만 보여준다.

> Ex) $ git log master..branchA
> Ex) $ git log origin/master..HEAD

#### `$ git log <branchA> <branchB> ^<branchC>`
#### `$ git log <branchA> <branchB> --not <branchC>`

branchA, branchB 에는 있지만 branchC에는 없는 commit을 보여준다.

#### `$ git log <branchA>...<branchB>`

서로 다른 commit만 보여준다.

---

#### `$ git log --all`

--all option을 추가하면 모든 log를 보여준다.

---

#### `$ git log --abbrev-commit`

--abbrev-commit option을 추가하면 짧고 중복되지 않는 hash값을 보여준다. 기본 7자를 보여주고, 중복될 경우 더 길게 보여준다.

---

#### `$ git log --decorate[=short|full|auto|no]`

--decorate option을 추가하면 log에 추가 정보를 보여준다.

---

#### `$ git log --graph`

--graph option을 추가하면 간단한 ascii graph를 보여준다.

---

#### `$ git log --oneline`

--oneline option을 추가하면 간략한 정보를 한 줄로 나타낸다.

`--pretty=oneline --abbrev-commit`과 동일하다.

---

#### `$ git log -#`

-# option을 추가하면 최근 #개의 commit만 보여준다.

---

#### `$ git log --follow <file>`

Continue listing the history of a file beyond renames (works only for a single file).

---

#### `$ git log --format:'%h - %s'`

--format option을 추가하면 원하는 형태로 보여준다.

* %H : Commit hash
* %h : Abbreviated commit hash
* %T : Tree hash
* %t : Abbreviated tree hash
* %P : Parent hashes
* %p : Abbreviated parent hashes
* %an : Author name
* %ae : Author email
* %ad : Author date
* %ar : Author date, relative
* %cn : Committer name
* %ce : Committer email
* %cd : Committer date
* %cr : Committer date, relative
* %s : Subject

---

#### `$ git log -p`

-p option을 추가하면 각 commit의 diff 결과를 보여준다. 즉, commit에 적용된 patch를 보여준다.

---

#### `$ git log --stat[=<width>[,<name-width>[,<count>]]]`

--stat option을 추가하면 각 commit의 통계 정보를 보여준다.

#### `$ git log --stat -M`

Show all commit logs with indication of any paths that moved.

---

#### `$ git log --shortstat`

--shortstat option을 추가하면 수정한 file, 추가된 line, 삭제된 line만 보여준다.

---

#### `$ git log --name-only`

--name-only option을 추가하면 수정된 file 목록만 보여준다.

---

#### `$ git log --name-status`

--name-status option을 추가하면 수정된 file의 목록에 추가, 수정, 삭제 여부도 보여준다.

---

#### `$ git log --relative-date`

--relative-date option을 추가하면 상대적인 시간을 보여준다. `--date=relative`와 동일하다.

---

#### `$ git log --since=<date>`
#### `$ git log --after=<date>`

--since, --after option을 추가하면 명시한 날짜 이후의 commit만 보여준다.

> Ex) $ git log --since=2.weeks

#### `$ git log --until`
#### `$ git log --before`

--until, --before option을 추가하면 명시한 날짜 이전의 commit만 보여준다.

---

#### `$ git log --author=<pattern>`

--author option을 추가하면 입력한 author의 commit만 보여준다.

#### `$ git log --committer=<pattern>`

--committer option을 추가하면 입력한 committer의 commit만 보여준다.

---

#### `$ git log -- <pathspec>`

-- option을 추가하면 파일 혹은 디렉토리가 변경된 log를 보여준다.

---

#### `$ git log -g <branch_name>`

-g option을 추가하면 reflog 정보도 볼 수 있다

---

#### `$ git log --left-right <branchA>...<branchB>`

--left-right option을 추가하면 각 commit이 어느 branch에 속하는지도 보여준다.

---

#### `$ git log --oneline --left-right --merge`

--merge option을 추가하면 충돌이 발생한 file이 속한 commit만 보여준다.

---

#### `$ git log -S<pattern> --oneline`

-S option을 추가하면 해당 문자열이 추가된 commit과 없어진 commit만 보여준다.

> Ex) $ git log -SZLIB_BUF_MAX --oneline

---

#### `$ git log -L <pattern>`

-L option을 추가하면 해당 함수나 line의 history를 보여준다.

> Ex) $ git log -L :git_deflate_bound:zlib.c

---

#### `$ git log --grep <pattern>`

--grep option을 추가하면 commit message 안에서 검색을 한다.

---
