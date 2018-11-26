Git Notes 6: Navigation

git log( simply shows all log)
if there too many logs in the screen you ll see two more pages /something searches something keyword in commit messages
git log —oneline(shows log in one line)
git log 3( shows last three commit)
git log 3 —oneline
git log —decorated(shows branch and head info in the log )
git log -S“something”( searches something in the content)
git whatchanged(show for each each commit which files changed)
git whatchanged —since=last.week
git notes add(add a note to a spesific commit)

git cat-file -p hashcode(show us what inside in hashcode)
git cat file -t hashcode(what simply done)
git show hashcode(shows what changed)
git show hashcode:/something

git show-branch( show changes in branch)
git diff hash1 hash2 ( diff bw twos. branch1 should be last)
git diff —word-dif  hash1 hash2 (show words change until space)
git diff —color-change hash1 hash2( show words change without braket)

git blame filename(who change it)
git gui blame filename( show change in gui)


