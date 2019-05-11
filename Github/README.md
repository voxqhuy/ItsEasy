Git

Connect local repo to GitHub: 
git remote add origin https://(url).git

BRANCH
Git branch : check branch
Git branch <branchA>  + Git checkout <branchA> = git checkout -b <branchA>
Git branch -f <branchA> <destination> : force moving branchA to a destination		Ex: git branch -f master HEAD~2

Git cherry-pick C3 C4 C7 : append commits C3 C4 C7 ahead the current HEAD

Git rebase -i HEAD~4 : allow to re-order the 4 commits before HEAD
Git rebase <branchA> <branchB> : append branchB to branchA		<moving branch> : default HEAD

Git commit --amend: update the most recent commit

Git tag v1 <branchA> : tag branchA as v1	<branchA> : default HEAD

Git describe <ref> : describe where you are relative to the closest ancestor tag		<ref> : default HEAD
=> result: <tag>_<numCommits>_g<hash> : <tag> is the closest ancestor tag, numCommits is how many commits away that tag is, hash is the hash of the commit being described

FETCH
Git fetch: point origin/.. to the right place locally (technically update remote’s pointer on local)
git push <remote> <place>
git fetch origin <source>:<destination>
git fetch origin :<destination> : create destination

Git pull = fetch + merge
Git pull --rebase = fetch + rebase

PUSH
Git push: push changes/update remote
git push <remote> <place> : update local to have all commits of <place> branch from <remote>		Ex: git push origin master
git push origin <source>:<destination>
git push origin :<destination> : delete destination		EX:  git push origin :foo will delete foo

git checkout -b totallyNotMaster o/master : Creates a new branch named totallyNotMaster and sets it to track o/master.
OR
git branch -u o/master <branchA> : will set branchA to track o/master		<branchA> : default HEAD


Merge VS rebase
Merge keeps the history; rebase makes it look clean (1 line)

Link a local repo with GitHub
git init
(git commit -m "first commit”)
git remote add origin https://github.com/kohnewlife/CPTR302-Firmware.git
(git push -u origin master)


