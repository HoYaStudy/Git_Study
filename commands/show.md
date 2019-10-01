# Show

각종 정보를 보여주는 명령어이다.

---

#### `$ git show <object>`

각종 정보를 보여준다.

> Ex) $ git show branch_A

> Ex) $ git show v1.0

---

#### `$ git show <object>@{n}`

규칙을 적용하여 정보를 보여준다.

> Ex) $ git show HEAD@{5}

* HEAD에서 5번째 전 정보

> Ex) $ git show master@{yesterday}

* 어제 master branch가 가리키던 정보

> Ex) $ git show HEAD@{2.months.ago}

* 2달 전에 HEAD가 가리키던 정보

---

#### `$ git show <object>^n`

n번째 부모의 정보를 보여준다.

> Ex) $ git show HEAD^

> Ex) $ git show HEAD^2

* 2번째 부모가 있는 merge commit에만 사용할 수 있다.

---

#### `$ git show <object>~n`

n번째 부모의 부모 정보를 보여준다.

---
