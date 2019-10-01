# Clone

Remote 저장소를 복제해서 local 저장소를 만드는 명령어이다.

Git의 저장소를 만드는 명령어 중 하나이다.

---

#### `$ git clone <url>`

자동으로 local 저장소의 master branch가 remote 저장소의 master branch를 추적하게 한다.

실제로는 directory를 만들고 그 directory에서 빈 저장소를 만든다. (`init`)

그리고 입력한 url로 origin이라는 이름의 remote 저장소를 추가한다. (`remote add`)

다음으로 remote 저장소에서 data를 가져온다. (`fetch`)

마지막으로 마지막 commit으로 working directory에 checkout 한다. (`checkout`)

---

#### `$ git clone -o <remote> <url>`
#### `$ git clone --origin <remote> <url>`

-o option을 주면 remote 저장소의 이름을 지정한 이름으로 복제한다.

---

#### `$ git clone --bare <directory> <repository>`

--bare option을 추가하면 directory의 .git directory 데이터를 bare 저장소로 복제한다.

---
