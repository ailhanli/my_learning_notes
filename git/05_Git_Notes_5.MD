Git Notes 5

Branching Recap
Branch gives us to chance to parallel development with temporary isolation. We develop new feature in new branch which is isolated from all other things happen.
After all, we will merge back in after we finish our job for a feature.

Merge
Git detech file change but not track it. It only tracks content change
If we change file name in two different branch without change their content after merge it will be two different file which are new files actually because git is not tracked file.

git log -1 --summary (get commit log for last commit with detail.)
git log --follow filename( show files history)
git log -M -p(show history if there is renaming and content change)

when we rename a file manual git cant detect, but it is not same if we change content. Thats because git detect and track content changes.

for text content changes, we have to solve conflict my hand, for the binary it is not easy we can use something like override and replace
For binary check
git log —merge -left-to-right
For override and replace
git checkout —theirs

Rebasing
Git rebase actually kind of merge.It solves same problem.It changes history. 
If we call git rebase master, it means rebase our branch from last version of master

git checkout master
git merge branch-1
is equas
git merge master branch-1

Git creates new commit for upcoming merge but it doesnt change branch anyway. if merging branch is so attractive, because of merge commit for every merge history pollution will occur and it is not easy to read. If we use rebase we rewrite branch history so it can be destructive but clean to read in case merging branch is so attractive.

