Git Notes 3

recap

git init(which will allows us to create new repository)
git add(that allows us to place new files into staging area or make to file changes in staging area 
git commit: which allow us to move whatevers in the staging area in to our repository area as a new set of changes and remember this doesnt override previous changes necessary in to repository and we can always get back any of the files in any commit)
 --Git add command overrites whatever into staging area, git commit will create a new log withing a repository. So we can jump from one commit to another

git status(which allows us to view current status of staging area whether there are things changed into working directory are reflected into staging area or whether there are things  in staging are which havent been committed)

git diff(that allows us to compare files from working directory with the staging area and we can used the cached flag to compare with the last commit
git log: which give us list of commits we made in git we call this log messages. It is actually current status of workplace)


How to manage changes middle of the commit.

git log —oneline (single line show commit)

--undo from stash
git reset HEAD(remove changes from staging are that is going to process. all the changes on staging are will be undone)
or 
git reset notes.txt(only the notes.txt will be undone)
git checkout notes.txt(it will get notes.txt from repository tp working directory
git status:
red things: which are in working area not in repository, it is going to commit.
green things: which are going to commit 

git ls-tree HEAD(what is in the last commit. HEAD means last commit)

git clone repository_name new_dir(copy repository in new directory)
--undo from repo
git revert HEAD(revert last commit. We can use hashcode 4 chars istead of HEAD)


--stashing
git stash(pause current set of work. current set of work will saved and current work space will return back to last commit)
git stash pop( get last stashed changes from stash area)
git stash list(list all stashed changes)
git stash drop( drop last stashed changes)

--partial commiting
git add --patch fileName(adding partial to commit. you can use ? for help, S for split chunks and then say T for sending part, F for not want)
