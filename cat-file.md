Each commit has a unique identifier called a `commit hash` a long string of character that identifies a commit ex.`5ba786fcc93e8092831c01e71444b9baa2228a4f` 
we can use first 7 chars to identify(`in a small repo`).

* use git log to find the `commit hash` of the commit you want to look into, 
* use cat-file to see the info of that commit
```bash
git cat-file -p 1c204093b
# 1c204093b -> first some char of of commit hash 
```

```stdout
tree 4a28d76324da1a866e8311fab3d8ff076a10aaf2
author Prince2412k2 <prince2412001@gmail.com> 1724500770 +0530
committer Prince2412k2 <prince2412001@gmail.com> 1724500770 +0530
```

* it gives us tree,blob,author,committer
* Tree -> committed folder
* Blob -> committed file
* author -> creator of the file
* committer -> who changed and committed file

we can look into any of them lets look into the tree
```bash
git cat-file -p 4a28d76
## 4a28d76 -> first some chars. of tree 
```

```stdout
100644 blob d2a91e385d14fd844d3c12e98377f3eafd44fcc3    boot.sh
100644 blob 442bd4fe6ee98bef43a977a27349f9b4dd9a64b9    contents.md
100644 blob ccc3e7b48da0932cc0f7c4ce7b4fd834c7032fe1    one.md
040000 tree e41bef46886bf10efe405908e9a1d87207b8e45d    quotes
100644 blob 742ae47550048eceeb91822826d4e6bca55fb897    titles.md
```

we can look into these blobs, lets look into boot.sh
```bash
git cat-file -p d2a91e385d1
## d2a91e385d1 -> first some chars. of blob boot.sh 
```

```stdout
#!/bin/bash
echo "hello world"
```

blobs contain the committed changes.

plumbing tools let you work directly with `.git` folder, at least very close to it. at a low level