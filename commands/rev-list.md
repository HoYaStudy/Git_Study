# Rev-List

List commits that are reachable by following the parent links from the given commit(s), but exclude commits that are reachable from the one(s) given with a `^` in front of them. The output is given in reverse chronological order by default.

A special notation `<commit1>..<commit2>` can be used as a short-hand for `^<commit1> <commit2>`.

Another special notation is `<commit1>...<commit2>` which is useful for merges. The resulting set of commits is the symmetric difference between the two operands.

---

#### `$ git rev-list <commit>`

Lists commit objects in reverse chronological order.

---

#### `$ git rev-list --left-right <commit>`

Mark which side of a symmetric difference a commit is reachable from. Commits from the left side are prefixed with `<` and those from the right with `>`. If combined with `--boundary`, those commits are prefixed with `-`.

---

#### `$ git rev-list --count <commit>`

Print a number stating how many commits would have been listed, and suppress all other output. When used together with `--left-right`, instead print the counts for left and right commits, separated by a tab. When used together with `--cherry-mark`, omit patch equivalent commits from these counts and print the count for equivalent commits separated by a tab.

> Ex) $ git rev-list --left-right --count master...origin/master

---
