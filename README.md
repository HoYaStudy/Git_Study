# Git_Study

This repository is for HoYa's git study.

Git은 분산 버전 관리 시스템이다.

---

## Installation

### MAC

> $ brew install git git-lfs

### Linux (Ubuntu)

> $ sudo apt isntall git git-lfs

### Windows

> $ choco install git git-lfs

---

## The Three State

Git은 file을 *committed*, *modified*, *staged*의 세가지 상태로 관리한다.

* *committed* : File이 local database에 안전하게 저장된 상태.
* *modified* : 수정한 file을 아직 local database에 commit 하지 않은 상태.
* *staged* : 수정한 file을 commit할 것이라고 표시한 상태.

`.git` directory는 git이 project의 metadata와 객체 database를 저장하는 곳을 말하며 git의 핵심이다.

.git directory에 있는 file들은 committed 상태이다. File을 수정하고 staging area에 추가했다면 staged 상태이다. Checkout한 후 수정했지만 아직 staging area에 추가하지 않았다면 modified 상태이다.

Working directory는 특정 version을 checkout한 것이다. .git directory는 현재 작업 중인 disk에 있고, .git directory안에 압축된 database에서 file을 가져와 working directory를 만든다.

Staging area는 .git directory안에 있으며, commit할 file에 대한 정보를 저장한다.

Git이 하는 일은 기본적으로 다음과 같다.

1. Working directory에서 file을 수정한다.
2. Staging area에 있는 file들을 stage해서 commit할 snapshot을 만든다.
3. Staging area에 있는 file들을 commit해서 .git directory에 영구적인 snapshot으로 저장한다.

---

## The Three Trees

### HEAD

현재 branch를 가리키는 pointer이며, branch에 있는 commit 중 가장 마지막 commit을 가리킨다.

### INDEX

다음에 commit할 내용이다. 즉, staging area를 가리킨다. 엄밀히 말하면 tree구조는 아니다.

### Working Directory

현재 사용자가 작업하는 file이 있는 곳을 가리킨다.

---

## Life Cycle

[Recording Changes to the Repository](https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository)

---

## Protocol

Local 저장소와 remote 저장소간의 data 전송에 사용되는 protocol은 4가지로 나눌 수 잇따.

### Local

Local file system을 사용하는 가장 간단한 방식이다. 외부 접속이 느리고 어렵다는 단점이 있다.

> $ git clone /opt/git/project.git
>
> $ git clone file:///opt/git/project.git

### HTTPS

사용자 이름과 비밀번호 방식으로 인증을 한다.

익명 사용과 인증 사용 모두 가능하다.

> $ git clone https://example.com/project.git

### SSH

설정이 쉽고, 보안에 안전하며, 전송 시 data 압축을 하기 때문에 효율적이다.

익명 접근이 불가능하므로 open source project 같은 경우 어려움이 있다.

> $ git clone ssh://user@server/project.git
>
> $ git clone user@server:project.git

### Git

9418 port를 사용하는 git에 포함된 daemon을 사용하는 것이다.

인증 및 보안이 없으며, 전송 속도가 가장 빠르다.

> $ git clone git://example.com/project.git
>
> $ git clone git@example.com/project.git

---

## Workflow

Branch를 활용한 workflow 3가지 예를 살펴보자.

### Long-Running Branch

Test를 거친 안정적인 배포 가능한 code만 master branch로 관리하는 방법이다.

개발 혹은 issue debugging, patch 작업 등은 별도의 branch에서 작업 한다.

### Topic Branch

특정한 작업을 위하여 branch를 만들어 관리하는 방법이다.

Issue debugging, hot fix 작업 등을 별도의 branch로 만들어 작업한다.

### Remote Branch

팀원과 함께 작업을 할 때 각자의 branch로 작업을 한 후, master branch를 동기화 하는 방법이다.
