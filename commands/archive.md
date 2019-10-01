# Archive

Source code를 배포할 때 사용하는 명령어이다.

---

#### `$ git archive <branch_name> --prefix=<prefix>`

source code의 압축 파일을 만든다.

--prefix option을 추가하면 file에 prefix를 붙여준다.

> Ex) $ git archive master --prefix='project/' | gzip > `git describe master`.tar.gz

> Ex) $ git archive master --prefix='project/' --format=zip > `git describe master`.zip

---
