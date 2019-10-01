# Remove Committed File

과거의 commit에서 특정 file을 삭제하는 방법이다.

> $ git filter-branch --index-filter \
>		'git rm --cached --ignore-unmatch ' \
>		--tag-name-filter cat -- --all
