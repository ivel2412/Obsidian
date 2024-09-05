lets create an environment for practice 
```bash
mkdir git_practice
cd git_practice
touch one.md two.md
```

## `init`
-> to initialize the repository
```bash
git init
```

output->`Initialized empty Git repository in path/to/your/dir/.git/`
***
## `add`
-> to add files to a staging area
here `.` represents all files and folders in current folder
```bash
git add .
```
***
## `stage`
-> shows files added to the stage
here `.` represents all files and folders in current folder
```bash
git status
```

```stdout
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   boot.sh
        new file:   contents.md
        new file:   one.md
        new file:   quotes/dune.md
        new file:   quotes/starwars.md
        new file:   titles.md
```
***
## `commit`
-> Commits all staged files to the Repo. 
```bash
git commit
#OR
git commit -m "First commit"
```
Here when we commit it opens a text editor where we can write down our commit message
if we use -m argument we can directly write that message
```stdout
[main (root-commit) 1c20409] first commit
 6 files changed, 41 insertions(+)
 create mode 100644 boot.sh
 create mode 100644 contents.md
 create mode 100644 one.md
 create mode 100644 quotes/dune.md
 create mode 100644 quotes/starwars.md
 create mode 100644 titles.md
```
***
## `log`
-> Commits all staged files to the Repo. 
```bash
git log
git --no-pager log -n 10 -graph
##you can use multiple arguments to decorate the stdout
```

```stdout
commit 1c204093bdc3104408e24df0ad4c4c865239a7f8 (HEAD -> main)
Author: Prince2412k2 <prince2412001@gmail.com>
Date:   Sat Aug 24 17:29:30 2024 +0530

    first commit
```
***
These 5 commands are mostly used and simple to understand

**edit code -> add it to stage -> commit it -> check log -> repeat**

other commands are less used and also more complex

### **`Other commands`**

[[Branch]]
[[Merge]]
[[Rebase]]
[[Reset]]
[[Remote]]commands