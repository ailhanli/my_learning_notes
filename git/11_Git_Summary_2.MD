Git Summary Part2

Git rebase command makes clean history. functionality is same as merge. in merge commit git creates new commit for every new merge. Merge causes "merge buble" which makes hard to read history.
ex:
git rebase hash 
or 
git pull --rebase

Git commit --amend, git reset --soft or --hard is potentially dangereous. Thats because they change tracking history. If we have already push our commit to remote for people work, it will be big problem if they use our old commit which is junk currently.

Recap:
We have three places to work. First is working directory, second is stashing area which is known as index and last one is repository
to move between commits use git reset if you havent already push your changes.

In case we want to make clean history via reset and then we will need cherry pick. 
cherry pick is also dangerous thats because if we pick wrong commit, it will be very big problem for us.

git revert commit is safe. Thats because it create new commit for every revert. Thats why it is totally safe to use even we have already pushed it.

git init creates working tree but git clone --bare creates remote repository.
bare repository is a remote repository where you can only push or pull. In bare repository there is no working files, index and stashing area. and also there is no .git folder. 

In case you want to create bare repository from working tree.
first use git clone --bare
then remove remote which is working tree. git remote rm origin.
then use git config receive.denyNonFastForwards true
then set out working tree remote using git remote add origin address
in case you push something from master not a branch you have to run git push --set-upstream origin master

git push or git pull is has default behaviour in case doing work from master to master.
but you have use git push /pull origin branch_name