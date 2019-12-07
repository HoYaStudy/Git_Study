# Prune

This runs `git fsck --unreachable` using all the refs available in `refs/`, optionally with additional set of objects specified on the command line, and prunes all unpacked objects unreachable from any of these head objects from the object database. In addition, it prunes the unpacked objects that are also found in packs by running `git prune-packed`. It also removes entries from `.git/shallow` that are not reachable by any ref.

---

#### `$ git prune`

Prune all unreachable objects from the object database.

---

#### `$ git prune -n`
#### `$ git prune --dry-run`

-n (--dry-run) option: Do not remove anything; just report what it would remove.

---

#### `$ git prune -v`
#### `$ git prune --verbose`

-v (--verbose) option: Report all removed objects.

---

#### `$ git prune --progress`

--progress option: Show progress.

---

## Notes

In most cases, users will not need to call `git prune` directly, but should instead call `git gc`, which handles pruning along with many other housekeeping tasks.

For a description of which objects are considered for pruning, see `git fsck`'s `--unreachable` option.
