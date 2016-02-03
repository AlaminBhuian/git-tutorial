Git Tutorial
============
A dummy repository to let other learn how to behave with git. It's just a short-form record. :)

### Tutorial
1. [গিট ব্যবহারের একেবারে প্রাথমিক জ্ঞান পর্ব ১ - tuts nano](http://tuts.nanodesignsbd.com/basics-of-git-1/) (Bengali : `bn_BD`)
2. [গিট ব্যবহারের একেবারে প্রাথমিক জ্ঞান পর্ব ২ - tuts nano](http://tuts.nanodesignsbd.com/basics-of-git-2/) (Bengali : `bn_BD`)

### Install git
> http://git-scm.com/downloads

Download and Install.

---

### Configure git

```
git config --global user.name "Someone"
git config --global user.email "someone@example.com"
```

---
### Start git

```
mkdir GitTest
cd GitTest								# enter the project directory
git init								# initiate git
touch README (mate README?)
git add README							# stage the file and its changes
git commit -m "first commit message"	# commit with a message
git remote add origin https://github.com/try-git/try_git.git 	# HTTP origin
git remote add origin git@github.com:the_user/g.git 			# SSH origin

```

---
### Collaborate with git

```
cd existingrepository
git remote add origin git@github.com:the_user/g.git
git push -u origin master				# push local commits to the cloud
git remote -v               			# a list of a Git project's remotes

git fetch								# fetch server changes to local repo *(but do nothing)*
git merge origin/master     			# merge the fetched changes to the master
git fetch && git log ..origin/master    # fetch server changes, and show the commit message
git log -p HEAD..FETCH_HEAD             # fetch server changes, show differences local-vs-remote
git pull                                # get and merge all the server changes

git show HEAD               			# see the HEAD commit
git checkout HEAD filename  			# restore the file to the last commit
git reset HEAD filename     			# unstage that file from the staging area
git reset 5d69206           			# rewind to the specified SHA commit *(first 7 chars. of the 40 char SHA code)*
```

---
#### Git tags

```
git tag -a v1.2 9fceb02					# mark with tag to a specific commit
git tag									# show the list of tags
git push origin --tags					# push all the tags to remote server
```

---
#### Git stash

```
git stash								# store changes in a dummy local storage
git stash list							# check the stashed dummy commits
git stash clear							# clear all the stashed dummy commits
```

---
#### Git branching

```
git branch 								# Check the branches

git branch branch_name					# Make a new branch
git checkout branch_name				# Get to the new branch
git checkout master						# Get back to the master branch
git checkout -b branch_name				# Shorthand: Create new branch and move onto it

git push origin branch_name 			# push your branch up, to the remote, origin

git merge branch_name 					# Being in `master` merging new branch to `master`

git branch -d branch_name				# Delete local branch
git push origin :remote_branch_name		# Delete a remote branch
```

---
### Git Local Sharing and Local Server setup

```
git --bare init                                           # instead of init it will create a base, not a repo
git remote add origin file:////pc65/test-directory        # local access to the folder required
```

---
