It lets you keep track of different changed separately

imagine you have a big project and you want to implement a new feature or want to experiment with some changes without changing the main code base, You can create  a **branch**.

its like a parallel universe for your code. where the main code is still unaffected and can be continued to be developed.
ex.
![[Pasted image 20240827121838.png]]
here `Master` is the main branch and `color_scheme` is new branch

## **Visualize branches**
```
       G - H    branch_three
      /
A - B - C - D   main
  \
   E - F        branch_two

main         -> A-B-C-D
branch_two   -> A-E-F
branch_three -> A-B-G-H

```

Use `git branch` to get all branches and which branch you are on and `git switch` to change branch

```bash
git branch
```

```stdout
* color_scheme
  main
```
current branch is showed with `*` 

## **More Commands**
```bash
git branch -m oldname newname # Change branch name

git branch name # Create New Branch 

git switch branch_name # Change current branch

```
