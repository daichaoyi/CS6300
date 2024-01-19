git checkout can be understood as moving the pointer to the branch. For example, git checkout development, means we move the pointer to the development branch, 
then the next commit will move the development branch only, the main will stay the same. 

* pull the branch,then modify, then push.
git pull origin development
* Create a file called dev2.txt that contains the text "Dev 2 file".
echo "Dev 2 file" > dev2.txt
* Commite the file to your local local repo (it should be in branch "development") with comment "Aded dev 2 file"
git add dev2.txt 
git commit -m "Added dev2 file"
git push origin development


Conflict: when a file was modified in local and remote repository, and the modification was different. When we push the local repository to the remote repository, there will be 'conflict', then we must modify either the local or the remote repository to make them consistent before push the local to the remote. 
[
](https://www.youtube.com/watch?v=5BwYTMVSPSk)https://www.youtube.com/watch?v=5BwYTMVSPSk
