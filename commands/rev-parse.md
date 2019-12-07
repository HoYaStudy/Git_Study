# Rev-Parse

---

#### `$ git rev-parse`

Pick out and massage parameters.

---

#### `$ git rev-parse --is-inside-work-tree`

When the current working directory is inside the work tree of the repository print "true", otherwise "false".

---

#### `$ git rev-parse --abbrev-ref[=(strict|loose)]`

A non-ambiguous short name of the objects name. The option core.warnAmbiguousRefs is used to select the strict abbreviation mode.

> Ex) $ git rev-parse --abbrev-ref HEAD

---

#### `$ git rev-parse --show-toplevel`

Show the absolute path of the top-level directory.

---
