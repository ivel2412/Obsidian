Used to undo commits

## Soft Reset
(default reset)
keeps the changes and deletes commits after given point
```
a-b-c-d-e-f
#let these be commit ids
```
if we soft reset to `c`
```bash
git reset c
```
output
```
a-b-c*
```
we will still have the same code as before but commits will be deleted
use it when you mistakenly commit something

## Hard Reset
also deletes the the changes in code. reverts everything back to given commit
```bash
git reset --hard COMMITHASH
```
this will modify the files to match the given commit hash