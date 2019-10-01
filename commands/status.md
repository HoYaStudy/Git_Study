# Status

git의 현재 상태를 보여주는 명령어이다.

---

#### `$ git status`

현재 상태를 보여준다.

---

#### `$ git status -s`
#### `$ git status --short`

-s (--short) option을 추가하면 현재 상태를 간략하게 보여준다.

---

#### `$ git status -b`
#### `$ git status --branch`

-b (--branch) option을 추가하면 현재 branch와 tracking 정보를 간략하게 보여준다.

---

#### `$ git status --show-stash`

--show-stash option을 추가하면 현재 stash 되어 있는 entry의 개수를 보여준다.

---

#### `$ git status -u[mode]`
#### `$ git status --untracked-files[mode]`

-u (--untracked-files) untracked file들을 보여준다.

- `no` : untracked file들을 보여주지 않는다.
- `normal` : untracked file들과 directory들을 보여준다.
- `all` : untracked directory들 안의 개별 file들도 보여준다.

---
