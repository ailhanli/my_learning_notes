
Git Notes 7: Rewriting History

It sounds like you shouldnt never do! B
Purpose of configuration management tool like GIT is to record sets of changes we make safely for pustarity.  In theory we shouldnt messy with history. But sometime you made mistake in commit message. 
Disturbited nature of git means that each person has copy of the repository. 

Golden History Rule:
Only change history you havent shared yet with someone else. It means you didnt pushed changes history can be changed. It means these changes not exist in their repository.
These are your changes and you are free to change them.
In contrast; Thats because you are changing history it will affect someone else job. It makes a lot of pain for someone who use you commit. Because when you want to change commit message you create new commit. 
Commit message creates from log message and branch name.
It is good idea if it is your repository and you didnt share yet. 

git reflog : all the changes made it to the tips of branch including head. When you make checkout reflog will record it. 
Log message is actually part of commit. This commit also includes branch-name.
git commit --amend -m "new message": create new commit because hash will changes
git reset --hard HEAD~1:  rollback one commit 

Recap:
At first we ca use --amend command in commit to change commit content. We did it just a chaneg to message It doesnt really change existing commit.
It cant because the hash depends on it is content sı if you change the content you going to get a new hash instead it removes the old commit leaving in the repository and add a new commit in place.
When we changing commit is change of fast forward mode thats because merge two branch can point to same commit.
Old commits stay in history but no any branch point them. 

If you havent share you commit you can ammend them. If you change commit message they change the hashcode. You end up with the completely new commit object. 
If you shared already create new commit to fix whatever you want  rather than change commit message. 

--Revert--Reset
Git revert HEAD: revert last commit via create new commit for this. it is safe
Git reset : dangerous for already commit. It is used for jumping in the tree.
	-by default mixed: revert staging area to working dir
	-soft: restaging already commited things to staging area. working dir is still same.
	-hard: reset all thing to working directory.
soft and hard is dangerous. Because they change 









