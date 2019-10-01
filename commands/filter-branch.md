# Filter-Branch

Branch를 재작성 하는 명령어이다.

---

#### `$ git filter-branch --tree-filter <command>`

--tree-filter option을 추가하면 history 전체에 command를 적용한다.

> Ex) $ git filter-branch --tree-filter 'rm -f passwords.txt' HEAD

---

#### `$ git filter-branch --commit-filter <command>`

--commit-filter option을 추가하면 특정 commit에만 command를 적용할 수 있다.

```sh
Ex) $ git filter-branch --commit-filter '
        if [ "$GIT_AUTHOR_EMAIL" = "hoya@localhost" ];
        then
          GIT_AUTHOR_NAME = "HoYa";
          GIT_AUTHOR_EMAIL = "hoya@example.com";
          git commit-tree "$@";
        else
          git commit-tree "$@";
          fi' HEAD
```

---
