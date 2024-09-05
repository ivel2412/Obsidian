Lets say you have 2 branches 
```
A - B - C    main
   \
    D - E    other_branch    
```

when you merge `main` and `other_branch` you combine these branches in a common commit
```
A - B - C - F    main
   \     /
    D - E        other_branch
```
here `F` is a merge commit

## commands

```bash
git merge other_branch # it merges the branch with current branch
# Ex.
# if we are on branch MAIN (current branch)
# we will merge other_branch into MAIN
git log --oneline --decorate --graph --parents
# use graph to se ASCI art of commits
```

```stdout
*   94d194e (HEAD -> color_scheme) Merge branch 'main' into color_scheme
|\
| * 558e618 (main) lamo
| * e1d9f37 what
* | e199fc1 hello
|/
* 1c20409 first commit
```
Each star represents commit
