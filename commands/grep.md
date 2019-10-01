# Grep

Commit tree 내용이나 working directory의 내용을 문자열이나 정규표현식을 이용하여 검색하는 명령어이다.

---

#### `$ git grep <pattern>`

Pattern으로 찾는다.

---

#### `$ git grep -n <pattern>`
#### `$ git grep --line-number <pattern>`

-n option을 추가하면 line 번호도 같이 보여준다.

> Ex) $ git grep -n gmtime_r

---

#### `$ git grep -c <pattern>`
#### `$ git grep --count <pattern>`

-c option을 추가하면 file별로 찾은 개수도 보여준다.

---

#### `$ git grep -p <pattern> <file>`
#### `$ git grep --show-function <pattern> <file>`

-p option을 추가하면 matching되는 line이 있는 함수나 method를 검색한다.

> Ex) $ git grep -p gmtime_r *.c

---

#### `$ git grep --and <patterns>`
#### `$ git grep --or <patterns>`
#### `$ git grep --not <patterns>`

--and option을 추가하면 여러 단어가 한 line에 나타나는 line을 검색한다.

---

#### `$ git grep --break --heading <pattern>`

--break option을 추가하면 matching되는 다른 file들 사이에 공백 line을 출력한다.

--heading option을 matching되는 곳 위에 file명을 보여준다.

> Ex) $ git grep --break --heading -n -e '#define' --and \( -e LINK -e BUF_MAX \) v1.8.0

---
