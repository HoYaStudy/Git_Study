# Clean

Remove untracked files from the working tree

---

#### `$ git clean -d`

`-d` : 하위 directory까지 적용한다.

---

#### `$ git clean -f`
#### `$ git clean --force`

---

#### `$ git clean -i`

Show what would be done and clean files interactively.

---

#### `$ git clean -n`
#### `$ git clean --dry-run`

Don’t actually remove anything, just show what would be done

---

#### `$ git clean -x`

`.gitignore`에 명시된 file도 삭제한다.

---

#### `$ git clean -X`

Remove only files ignored by `Git`.

---
