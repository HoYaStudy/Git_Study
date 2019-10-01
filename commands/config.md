# Config

Git을 설정하는 명령어이다.

## Scope

Git의 설정은 3단계의 scope를 갖는다.

* `system` : `/etc/gitconfig`
* `global` : `~/.gitconfig`
* `local` : `<project_root>/.git/config`

보통 모든 project에 공통적으로 적용할 설정은 global에 두고, project별로 적용할 설정은 local에 둔다.

우선 순위는 `local > global > system` 순이다.

## Configuration

---

#### `$ git config --list`

--list option을 추가하면 설정된 내용을 보여준다.

---

#### `$ git config --system <name> <value>`
#### `$ git config --global <name> <value>`
#### `$ git config --local <name> <value>`

--system, --global, --local option을 추가하면 각각의 scope에 해당 설정이 적용된다.

---

#### `$ git config --system --unset <name>`</name>`
#### `$ git config --global --unset <name>`</name>`
#### `$ git config --local --unset <name>`</name>`

--unset option을 추가하면 해당 설정을 제거한다.

---

#### user.name "UserName"

사용자 이름을 설정한다.

#### user.email "E-Mail"

사용자 e-mail을 설정한다.

#### color.ui *true*

Terminal 출력 결과에 색상을 입힌다.

* color.branch \<*true* / *false* / *always*\>
* color.diff \<*true* / *false* / *always*\>
* color.interactive \<*true* / *false* / *always*\>
* color.status \<*true* / *false* / *always*\>

#### commit.template <file>

commit할 때 명시한 file에 있는 내용을 자동으로 넣는다.

#### core.autocrlf *input*

개행문자를 설정한다. windows의 경우 *true*를 사용한다.

#### core.editor *nvim*

환경 변수에 설정한 편집기 대신 명시한 편집기를 사용한다.

#### credential.helper *osxkeychain*

git remote repository의 연결 암호를 저장한다.

* *osxkeychain* : MAC OSX의 key chain에 저장한다.
* *wincred* : windows에서 사용한다.
* *cache* : 15분간 저장한다.
* *store* : 텍스트 파일로 저장한다.

#### credential.username "UserName"

해당 git repository의 계정을 변경한다. 주로 --local옵션과 함께 사용한다.

#### help.autocorrect 1

명령어를 잘못 입력해도 자동으로 추측하여 실행한다.

#### merge.tool *p4merge*

Merge tool을 설정한다.

#### pull.rebase *true*

pull할 때 기본적으로 --rebase option이 적용되도록 설정한다.

#### push.default *simple*

push할 때 기본으로 현재 branch만 하도록 한다.

#### rerere.enabled *true*

reuse recorded resolution 설정이다. 충돌이 났을 때의 해결책들을 저장하고 있다가 동일한 문제가 발생했을 때 다시 적용해준다.

#### alias.\<name\> \<command\>

Alias를 설정한다.

> Ex) $ git config --global alias.unstage 'reset HEAD --'
>
> Ex) $ git config --global alias.last 'log -1 HEAD'
>
> Ex) $ git config --global alias.visual '!gitk'

---
