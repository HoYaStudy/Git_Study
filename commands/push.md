# Push

Local 저장소의 내용을 remote 저장소로 전송하는 명령어이다.

---

#### `$ git push <remote> <local_branch>`

remote 저장소에 local branch data를 전송한다.

> Ex) $ git push origin +master

+를 붙이면 error가 발생해도 무시하고 push한다.

---

#### `$ git push <remote> <local_branch:remote_branch>`

Local branch를 지정한 이름으로 remote 저장소로 전송한다.

---

#### `$ git push <remote> <tag>`

Tag는 자동으로 remote 저장소에 전송되지 않으므로, 직접 명시해야한다.

> Ex) $ git push origin v1.2

---

#### `$ git push --tags <remote>`

--tags option을 추가하면 remote 저장소에 없는 tag를 전부 전송한다.

---

#### `$ git push -d <remote> <branch>`
#### `$ git push --delete <remote> <branch>`

--delete option을 추가하면 remote 저장소의 branch를 삭제한다.

---

#### `$ git push -f`
#### `$ git push --force`

--force option을 추가하면 remote 저장소의 commit history를 새로 덮어쓴다.

---

#### `$ git push -u <remote> <local_branch> <remove_branch>`
#### `$ git push --set-upstream <remote> <local_branch> <remove_branch>`

-u option을 추가하면 local branch 사본을 remote에 전송한다.

---
