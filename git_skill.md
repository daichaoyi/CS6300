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

*  after using the git push origin main, it reports a conflict. When I open the local 'info.txt' file, I found that it reports the differece between the local and remote repository. Then use vi to make change. Notice that, I should not directly make change on the Github, becuase once I make the change, the commit ID will change. If I push later, it will not allow me to push. Therefore, just simply make change in the local repository. and then push.
<<<<<<< HEAD
sping24<my id>
=======
spring 2024
>>>>>>> feature-branch
Conflict: when a file was modified in local and remote repository, and the modification was different. When we push the local repository to the remote repository, there will be 'conflict', then we must modify either the local or the remote repository to make them consistent before push the local to the remote. 
[
](https://www.youtube.com/watch?v=5BwYTMVSPSk)https://www.youtube.com/watch?v=5BwYTMVSPSk


https://opensource.com/article/23/4/resolve-git-merge-conflicts


White Box Test
branch coverage technique:
Branch coverage technique is a whitebox testing technique that ensures that every branch of each decision point must be executed.

if (a<150)||(b<200){
  for (i=a, i<100, i++)
}

  
Condition —— a Boolean expression containing no Boolean operators：
<img width="851" alt="Screenshot 2024-03-16 at 6 15 30 PM" src="https://github.com/daichaoyi/CS6300/assets/50822172/bd34e991-d48f-42d5-9cf4-f4a4cdf17a40">

三、条件覆盖（Condition Coverage）

条件覆盖于分支覆盖不同，条件覆盖要求所设计的测试用例能使每个判定中的每一个条件都获得可能的取值，即每个条件至少有一次真值、有一次假值。

仍然以上面流程图作为例子来说明。上图中涉及到的条件一共有4个：

a>0, a<0, b>0, b<0

为了达到条件覆盖的目的，我们设计的用例需要在 a 点有：

a>0, a≤0, b>0, b≤0，

这些情况出现，并且在 c 点有：

a<0, a≥0, b<0, b≥0

这些情况出现。现在可以设计如下用例：

TestCase1: a=1, b=1    (路径：ab)

TestCase1: a=-1, b=-1    (路径：acd)

TestCase1: a=-1, b=0    (路径：ace)

TestCase1: a=1, b=-1    (路径：ace)

通常而言条件覆盖比判定覆盖强，因为条件覆盖使得判定中的每一个条件都取到了不同的结果，这一点判定覆盖则无法保证。但条件覆盖也有缺陷，因为它只能保证每个条件都取到了不同结果，但没有考虑到判定结果，因此有时候条件覆盖并不能保证判定覆盖。

Decision —— a Boolean expression composed of conditions and zero or more Boolean operators：
Modified Condition/Decision Coverage(MCDC) —— every point of entry and exit in the program has been invoked at least once，every condition in the program has taken all possible outcomes at least once，and each condition in a decision has been shown to independently affect a decision S outcome by varying just that condition while holding fixed all other possible conditions.MCDC: 






