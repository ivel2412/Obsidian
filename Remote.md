Remote repo is just another repo. it can be on the same computer or another
it can also be [[github]] .

`add`
```bash
git remote add <name> <uri>
# name can be any name
# uri is relative path to the remote repo
```

`fetch`
```bash
git fetch
# Downloads all files from remote repo
```

`log`
```bash
git log remote/branch
#Ex. 
git log origin/main
# to see remote repo's logs
```

`merge`
```bash
git merge remote/branch
# just as we merge branchs in local repo we can do it with remote repos as well
```
