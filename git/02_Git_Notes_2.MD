Git Notes 2

git hash-object filename(give us hashcode will be created if we add this fle to on repository)

git add . (add all files on the repository stashing area)

.gitignore files definition we can simply add *.class to ignore class files.

git rm file(delete file from both cache and disk)
git rm --cache file(remove file only from cache)

git cat-file -p 4hashcode(show us what is inside git snapshot binary file)


when we add files to on staging area git create snapshot for each. 
when we commit git create two files for commit one is for who commited and which file hash another is use this hash to show which files commited.

git show hashcode 4 chars ( show us what happened (everything) is in commit)

Git Add commend actually add content changes to repository not the file.


git diff(show us difference bw working dir and stashing area. it is meaninfull to see what we will stashing and we should call it before stashing)

git diff —cached(bw stashing and repository)
