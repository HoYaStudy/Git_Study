# Move Tag

Tag의 위치를 변경할 때 사용하는 방법이다.

1. Remote repository에서 해당 tag를 삭제한다.

```sh
$ git push origin :refs/tags/<tagname>
```

2. Tag를 현재 commit으로 강제로 옮긴다.

```sh
$ git tag -fa <tagname>
```

3. Remote repository에 tag를 올린다.

```sh
$ git push origin master --tags
```
