Git is Version control system

**Used for**
- Keep history of your code changes
- Revert mistakes in code
- collaboration
- Backup your code

The commands are divided into Two category
- **[[Porcelain Commands]]** (High Level)
- **[[Plumbing Commands]]** (Low Level)

When we initialize git in a folder it creates a `.git` file and we can call that folder a **Repository**, The `.git` folder keeps all the commits so if you delete it you will loose all your data.

### *User* 
Git can be configured at different levels ->
- **system**: `/etc/gitconfig`
- **global**: `~/.gitconfig`
- **local**: `.git/config`
- **Worktree**: `.git/config.worktree`
![[Pasted image 20240824182931.png]]

## **[[Branch]]**

- Branch are like parallel universe for your code, lets you experiment or develop new features without changing the current state
- it is like a copy of your code but its not the same as copy
- every branch is a pointer to a commit. check out the [[Branch]] note

## **[[Merge]]**

* Converting two branches together into a single commit

## **[[Rebase]]**

* Alternative to git merge 

## **[[cat-file]]**
- a plumbing command to read into commits

## **[[Reset]]**
* Used to undo the last commits

## **[[Remote]]**
