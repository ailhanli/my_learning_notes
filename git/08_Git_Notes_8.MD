Git Notes 7 Cherry Pick

merge buble 
it is sometimes bad because they make it hard to work out which commit cause which changes in the code.
they also cause your set of changes could be fragmented. which makes difficult to manage.

long branch need keep in sync, traditional merge each time you want to sync end up with circled merge bubble. 
it is complicated and obsecure the history.  So instead we have seen  how it might be possible to achieve simply 
history by only changes the top of state of the original branch we have seen how can it be done manually by roll back branch
git reset doing a fast forward merge from the original branch and then re-applying the changes on top of new state 
with cherry pick. This was fiddly to do and dangerous for example if   we forgot one of the changes.

That's the purpose of git rebase command. it automates this changes we have just done manually 
to roll them   back and fast forward starting  point and apply changes on top. It is alot straight forward
than by hand 
