Lets say we have a commit history like...
```
A - B - C    main
   \
    D - E    feature_branch
```

with `rebase` we can attach the first commit of `other_branch` to  last commit of `main`. Creating a commit history without any merge commits

```
A - B - C         main
         \
          D - E   feature_branch
```

similar to merge commit we will need to go to the branch we need to rebase on to main
Ex.
```bash
git switch feature_branch
```
then we can rebase it to whatever branch we want
```bash
git rebase main
```
