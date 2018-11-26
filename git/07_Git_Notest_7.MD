Git Notes 7 Reset

Reset simply means moving Head from one commit to another.

Git reset Head: it is default mixed mode. It simply reverts back changes from index to work dir. It is totally safe because there is no changes on repository commits.

Git reset —soft Head: it reverts back changes from repository to staging area. 

Git reset —hard Head^1:  it reverts all last things from everywhere. 

soft reset says i want to potentially minor modifications on my last of changes. 
hard reset says i want to revert previous point in time. 
both of them potentially dangerous if we have already pushed our commits to remote and shared with someone.