
# Version control Learning
Types of Version control systems:-
	Subversion
	Perforce
	AWS code commit
	Git
	Murcurial

Catergories:-
	Certralized Version Control Systems(Subversion,Concurrent Versions System)
	Distributed Version Control Systems(Git,Murcurial)

Stagging and Production:-

 The goal of Continuous Deployment is to deploy and release software to customers frequently and safely.
 The strategy commonly involves automatically deploying to a test (also known as staging) environment first 
to validate the deployment package and software changes. Once validated, it can automatically deploy to the 
live (also known as production) environment for customers.

Startgies used to implement Version control:-


	Workflow
	Continous Integration
	continous Delivery
	continous Deployment
 

Redirection:-
	There are three types of INPUT/OUTPUT redirection
		stdin(0) <
		stdout(1) >
		stderror(2) 2>


We can use both stdout and stderror:- 2>&1


Grep:-(Global Regular expression Print)
	it is used for seaching	files,folders,content in a file
grep -w
grep -i
grep



some new commands:-
less
touch
pwd
chmod
grep


How Git Works:-
	Git workflow(3 states)
		modified
		stagged
		committed


Q)You are working on a project and have to share some code with a colleague. 
What is the correct order the code will flow in Git workflow?     
    Working directory, staging area, committed files, remote repository  


clone,Add,commit:-

git clone url

git add:- it is used track the file and also that marks a file to be included
		as part of a code commit
git restore --staged filename:- it is used to revert the above commnd

git commit -m ""

git push :- to submit the local changes to the remote server.

note :- git add, commit will put the changes into staging area.Push will add them  remote



Branches:-

To create a new branch we have two commands

	git checkout -B nameofthebranch
	git branch nameofthebranch
Both commands will do the same but the key difference is that first command will move to new branch .
example:-
	git checkout -B feature/lesson
	touch test2.txt
	git add test2.txt
	git commit -m "file 2 added"
	git push -u origin feature/lesson
Note :- main and feature/lesson they are two isolated branches . so the updates will be local to 
	the newly created branch ,so we have to merge to the main branch inorder see the changes.
we get an pull request , now dev can compare the pull request and merge it to the main branch.


Clone and pull:=

	clone is done for the first time.
	pull is done when u want to get the latest changes to that repository.

Remote vs local:=
	To create a new repo locally 
		git init
	To connect this local repo to remote
		git remote add origin url
	To check whether local repo is connected to remote
		git remote -v
	To get the latest changes from the remote repo use
		git pull
	After this we have to set up the branch that matches the server repo(remote repo)
		git checkout main // This will setup main to track main in remote

Quiz:-
When you perform a Git Push command, it copies content from your local repository and then uses 
it to merge all of the content in the remote repository.   
Ans: False,  When you use Git Push, Git compares a snapshot of your local repository with the remote 
one and only replaces the files that have been changed.  


HEAD:-
It is like a pointer which points to the current working branch


Some commands:-
	To check which branch is currently we are working on
		git branch
	To move to the another branch
		git checkout branchname
	To confirm the above
		cat .git/HEAD
	To check which files have been changed
		git status
	To check what exactly have been changed
		git diff
	To check at what point , who, time,line changed
		git blame filename
	To check changes from specfic lines
		git blame -L 1,2 filename

Diff commands:-

	Diff can be used to compare file within ur local repos,commits and also branches.
	To compare files before the commit 
		git diff HEAD filename
	To compare between branches
		git diff branchname branchname
	To compare between commits 
		git logs --pretty=oneline //u get the hash codes for the each commit
		git diff hashcode hashcode
	
Forking:=
   Forking is another type of workflow. The key difference between branching and forking is that 
   the workflow for forking creates a new repository entirely. Branching cuts a new branch from the 
   same repository each time and each member of the team works on the single repository.

   Each repository will have its own guidelines for submitting PRs against them and usually provide a 
   how-to contribute guide. As you can see, in order to get the changes from our forked repository, 
   you need to compare it against the original. This gives a lot of control to the repository owners of the
   original and they get to decide what makes the cut to be merged in.


