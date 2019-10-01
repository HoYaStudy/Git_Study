# .gitignore

Git에서 관리하고 싶지 않은 file들을 명시하는 명령어이다.

## Usage

Git repository에 `.gitignore` file을 만들고 무시할 file의 pattern을 명시한다.

* Blank line, #으로 시작하는 line은 무시한다.
* 표준 glob pattern을 사용한다.
	+ *는 0개 이상의 문자를 의미한다.
	+ []는 안에 있는 문자 중 하나를 의미한다.
	+ ?는 문자 하나를 의미한다.
	+ **는 directory안의 하위 directory들까지 의미한다.
* /로 시작하면 하위 directory에 적용되지 않는다.
* Directory는 /를 끝에 붙여서 표현한다.
* !로 시작하는 pattern의 file은 무시하지 않는다.

## Example

```sh
# Ignore *.o, *.a files
*.[oa]

# Ignore *.a, Don't ignore lib.a
!lib.a

# Ignore TODO file only in the current directory
/TODO

# Ignore all files in the build directory
build/

# Ignore *.txt files in doc directory, Don't ignore *.txt files in the sub-directories
doc/*.txt

# Ignore *.txt files in doc directory and all sub-directories.
doc/**/*.txt
```
