# Git commands

## Basic Commands

- `git clone <Repository URL>`

> It will download a copy of the repository from the origin.
>
> **Ex:** `git clone https://github.com/bpaulo/cs50lecture0.git`


- `git add <filename>`

> It will put the file on tracking and include it on the repository in the next commit.
>
> **Ex:** `git add hello.html`


- `git commit -m <"comments">`

> It will take a snapshot of the repository in the current moment and save it.
>
> **Ex:** `git commit -m "Added hello.html and classNotes.md"`


- `git status`

> It will show what's the current status of the repository that you are working on at any given moment.


- `git push` 

> It will push the changes from the local computer to the origin.

- `git pull` 

> It will pull the lastest version from origin to the local computer.

- `git log`

> This command shows the history of all the commit that you've made. To quit `git log` type `q`
>
> **Ex:** `git log`
> 
>   `commit 58725f16aa1abc2ba7e4d7f2dc18ad462e0b7aff (HEAD -> master) `
>   `Author: Bruno Paulo <bpauloec@gmail.com>                         `
>   `Date:   Sat May 23 10:18:04 2020 -0300                           `
>   `                                                                 `
>   `    Added git pull command and third hello.                      `
>   `                                                                 `
>   `commit da1eb0733f3db6fa4be1d763f2582ba4c0fd2b47                  `
>   `Author: Bruno Paulo <bpauloec@gmail.com>                         `
>   `Date:   Sat May 23 10:04:47 2020 -0300                           `
>   `                                                                 `
>   `    Update hello.html                                            ` 

## Merge Conflicts

Merge conflicts happens when there are two or more changes in the same line of the same file. Git will show alerts about merge conflicts during pull and push requests. 

> **Ex:**
> Message after `git pull`:
> 
>   `Auto-merging hello.html`
>   `CONFLICT (content): Merge conflict in hello.html`
>   `Automatic merge failed; fix conflicts and then commit the result.`
> 
> How the file looks like during the conflict: 
```shell
a = 1
<<<<< HEAD
b = 2
=====
b = 0
>>>>> 57656c636ff6d6520746f20576562
c = 3
d = 4
e = 5
```
> 
> To resolve conflict the wrong piece of code needs to delete as the HEAD and HASH COMMIT lines. 
> ```shell
> a = 1
> b = 2
> c = 3 
> d = 4
> e = 5
> ```
