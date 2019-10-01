# Tag

태그를 만드는 명령어이다.

Git의 태그는 2 종류가 있다.

* Lightweight Tag: 특정 commit에 대한 포인터일 뿐이다.
* Annotated Tag: 태그를 만든 사람의 이름, 이메일, 생성일, 메시지도 함께 저장한다.

---

#### `$ git tag`

Tag 목록을 보여준다.

---

#### `$ git tag -l <pattern>`
#### `$ git tag --list <pattern>`

-l option을 추가하면 pattern이 일치하는 tag 목록을 보여준다.

> Ex) $ git tag -l 'v1.*'

---

#### `$ git tag <tag>`

Lightweight tag를 만든다.

> Ex) $ git tag v1.0

---

#### `$ git tag <tag> <commit>`

해당하는 commit에 tag를 붙인다.

---

#### `$ git tag -a <tag> -m <message>`
#### `$ git tag --annotate <tag> --message=<message>`

-a option을 추가하면 annotated tag를 만든다.

-m option을 추가하면 간단한 tag message를 작성할 수 있다.

> Ex) $ git tag -a v1.0 -m 'version 1.0'

---

#### `$ git tag -a <tag> <commit>`
#### `$ git tag --annotate <tag> <commit>`

해당하는 commit에 tag를 붙인다.

> Ex) $ git tag -a v0.7 9fceb02

---
