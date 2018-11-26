Git Notes Last —Remote Repositories

git clone repository new_name: cloning entire repository to your local. second param is optional
—only the tracked files will be cloned

git branch —list: list the branches locally
git branch —remotes: list the remote branches from local clone.

when cloning tags and unreachable object won’t cloned because of efficiency.
 
git config --local --add user.name "Clone User”: adding new user for current clone in order to understand who s changing.



Two stage process: first fetch then merge

git fetch: gets all changes from remote to local repository

git merge origin/master:  merges changes from origin/master which is get by fetch to local master

git pull = git fetch + git merge

git pull —rebase: fetch and then merge via rebase so history will changes. rebase equals clean history. otherwise you need to reset then pull and then cherry pick commit

**It is up to developer to use which one. first fetch and then check changes and then merge is good idea.



if we use directly merge in case of we want to revert back changes we use git reset origin/master

Push only updates repository not in index or working tree

git bush origin..HEAD: what we are actually check in. what is change bw origin and local

In case origin repository is someone local repository it will be a problem in case pushing branch is working tree and has index.

If you use github origin repository you don’t have any issue. github purely act as way of hosting remote repository for everybody. 

If you have a name of the branch your local repository matches name of the branch of remote repository they will effectively merge as part of push.







--Bare repository--

is a remote repository hasn’t either staging area orindex or working directory.

It is simply using for pushing and pulling to. No working is done directly against it. Because not working dir or index you never get error message we have already seen before when you push to bare repository.

In bare repository, there is no working files ör .git directory. 



git clone —-bare Countries/ countries-and-capitals.git: creating bare repository. name end with .git is high recommended. It is just a convention.

or

git init --bare: creates empty bare repository



--Because we cloned bare repository from a working tree, working tree will be origin of bare repository. so to delete it:

git remote rm origin: removing remote origin from bare repository.



--only allows if push in fast-forward mode. So you dont have conflict to deal with in your remote repository

git config receive.denyNonFastForwards true: it open bare repository for fast-forward merge which is no conflict in case of merge



--set the repositorys remote.

git remote add origin address: change our origin to address.******

git fetch: in order to know remote branches from bare repository. You will see that there is no head on remote. 



--setting remote HEAD thats because we have already lost HEAD!!!

git remote set-head origin -a: set origin of remote as master



--by default if you chaneg master branch you cant push. you have do changes in feature and then push or;

git push --set-upstream origin master



--setting a branch remote

git remote set-url origin url: setting remote url of current repository.



git push origin branch-name: push our branch to remote 


























