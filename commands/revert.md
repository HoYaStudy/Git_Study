# Revert

Revert some existing commits.

---

#### `$ git revert <commit>`

Create new commit that undoes all of the changes made in \<commit\>, then apply it to the current branch.

---

#### `git revert -m parent-number <commit>`
#### `git revert --mainline parent-number <commit>`

-m option을 추가하면 merged commit을 revert 한다.

> Ex) $ git revert -m 12f5a03

---

#### `$ git revert -n <last_commit_to_keep>..<newest_commit_to_reject>`
#### `$ git revert --no-commit <last_commit_to_keep>..<newest_commit_to_reject>`

-n option을 추가하면 여러 commit을 revert 하고, revert된 commit 하나당 하나의 객체를 생성하는 대신 하나의 revert commit을 생성한다.

---
