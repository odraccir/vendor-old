GitHub Command
================================

sends all the branches to [remote] repository
> git push [remote] --all
change the current branch to [branch]
> git checkout [branch]


Remote repository names

> $ git remote -v
> BitBucket       https://odraccir@bitbucket.org/odraccir/vendor.git (fetch)
> BitBucket       https://odraccir@bitbucket.org/odraccir/vendor.git (push)
> GitHub  https://odraccir@github.com/odraccir/vendor.git (fetch)
> GitHub  https://odraccir@github.com/odraccir/vendor.git (push)

Update repository and send new versions

> $ git pull {remotename} {master|branch}
> $ git push {remotename} {master|branch}

Update repository ignoring any discrepancy 

> $ git push {remotename} {master|branch} --force

Move all local modification on top of the master branch

> $ git pull --rebase {remotename} {master}

delete an unwanted branch

> $ git push origin --delete {branch}
> $ git push {remotename} {master|branch} --force 

Check modified files

> $ git status -s

Extract a file from a branch replace the actual file

> git checkout {branch} -- filename.ext

Go back a commit to {sha1} and reset master to point to {sha1}

> $ git reset --hard {sha1}
> $ git push {remotename} {master|branch} --force