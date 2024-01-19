git checkout can be understood as moving the pointer to the branch. For example, git checkout development, means we move the pointer to the development branch, 
then the next commit will move the development branch only, the main will stay the same. 


Conflict: when a file was modified in local and remote repository, and the modification was different. When we push the local repository to the remote repository, there will be 'conflict', then we must modify either the local or the remote repository to make them consistent before push the local to the remote. 
