
Git Notes 4 

branch is isolated parallel changes. changes on branch wont affect main branch.
it is actually duplicate the one or more objects allow us to independently work on copy which wont affect other. 
it is actually name pointer for particular commit. this pointer will change it. 
name shortcut for particular commit.

--go backward forward
git checkout HEAD~2(go two commit before)
git checkout master(return to master branch)

--branching
git branch -b branch-name(creating new branch. Name shouldnt contain space)
git branch --no-merged(get branches which didnt merged)
git merge branch_name(merge branch)
--creating a new branch all of actually does creating a ref object in our folder which is a tiny little fire. So does no much overhead to creating new branch in git. Thats why we encourage you creating many branch as we like.
different feature should have own branch


rules for branch name
for feature create feature/branch_name
for bug create bugfix/branch_name

creating branch is cheap and painless. creating branch simply means creating new ref object to branch which is base branch.

git commit -am file(add to stage and then commit changes of already exit file. for modification and deletion it can be used)
git checkout - ( go before branch we are in)
git checkout something master(it create new branch from master even we are in different branch currently)
git reset HEAD file(it will unstash the file.)

git show-branch(show what is going on in all branches)
--merging one branch to another is not recommended. thats why we create branches from master.

git branch --contains branch_name(which branch contains this branch name shows)
git tag hash_code 
git checkout branch or hashcode ~(go parent of last commit of branch or hashcode commit)
git checkout branch~2 (go parents of parent of last commit in branch)
git checkout branch^2(go same thing like carrot but via second parent)
git tag -f name_of_tag  branch_name or hashcode(force to move tag)

git checkout :/“kepp"(go to last recent changes who has keep word in commit message)

