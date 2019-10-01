# Rebase

Merge 명령어와 마찬가지로 commit을 합치는 명령어이다.

한 branch의 commit을 patch로 만들어 이를 다른 branch에 적용하는 방식이다.

Merge와 비교하여 최종 결과물은 같지만 commit history가 좀 더 깔끔해진다.

절대로 주의해야할 점은 "공개 저장소에 push된 commit을 rebase하지 말 것" 이다.

---

#### `$ git rebase <branch_name>`

현재 branch의 내용을 patch로 만들어 명시한 branch에 적용한다.

> Ex) $ git checkout branchA

> Ex) $ git rebase master

> Ex) $ git checkout master

> Ex) $ git merge branchA    // Fast-Forward

---

#### `$ git rebase <base_branch> <topic_branch>`

topic branch를 checkout하여 base branch에 적용한다.

> Ex) $ git rebase master branchA

> Ex) $ git checkout master

> Ex) $ git merge branchA

---

#### `$ git rebase --onto <newbase> <upstream> <branch>`

--onto option을 추가하면 다음과 같이 수행한다.
*	rebase할 branch를 checkout 하고, upstream, branch의 공통 조상 이후의 patch를 만들어 newbase branch에 적용한다.

---

#### `$ git rebase -i <commit>`
#### `$ git rebase --interactive <commit>`

-i option을 추가하면 대화형 mode로 수행한다.

> Ex) $ git rebase -i HEAD~3    // 마지막 3개의 commit을 수정한다.

---

#### `$ git rebase --continue`

--continue option을 추가하면 나머지도 동일하게 적용한다.

---
