Summarize Git Part-1

Two step adding changes to repository.
First you need to add changes to stashing area. It simply means adding snapshot of thins into git directory. Git creates hash code from content and keep snapshot with this hash code in git objects directory.
Second you can add snapshot to history which is simply commit command does.

 
Creating new branch means creating ref to existing branch for parallel isolated working.
In future you will need to merge it each other. 

There is two way for merge , first is merge which is create new merge commit for each merge. If merging branch is change more.It will be difficult to follow changes. On this time you can use rebase. But rebase change branch history it can be destructive. What i mean changing history, all hash codes of changes will be updated. It is more readable than merge in case of many merge

Git don't track files, it tracks content changes.

Head means where we are in the branch
add means index it, commit means put in the repository