Git Notes 1

git init(creates an empty repository)

git status(current status of repository. git creates master branch by default for working. this command also shows untracked files)

git add file(place file into the repository. after add command files in to repository)

--what we have done so far we say git we want to configure files on the disk but we havent yet actually added to the repository and we added into staging area which is intermediate step working files on the disk and confgured files stored on the git. 
two steps process to add file to git. 

Two stage process--
First step is git add. it take snapshot of file(s) and move it into staging area. Git now knows about file. Git takes permanent snapshot of file and allows us to them make subsequent changes and always to able to back to version we commited.

git commit -m(we added changes to repository via git add command. We added files to staging area via git add command. when we ready to commit. Everthing into staging area will be placed into repository aread after we commit)

Git knows who is doing the commit via using following to command in order to identify who we are.
git config --global user.email ""
git config --global user.name ""

Git keeps files via hashcode which is created from contents of files. If we want to find spesific commit we have to note this id and then we can return back to commit.
First 7 character is ok to do job. All commits have hashcode and it is created from content of file. 


git log( show us history of commits in detail)

git diff( we use this command to check changes between two version via hashcode(first 7 chars))


