Contribute notes based on [this](https://www.youtube.com/watch?v=SFLpVkF0obY&list=PL2kSRH_DmWVajYgFoP-HVKK5VKkzFYyzp&index=3) video now!

## Commit Objects
As we have studied earlier about committing changes, let's know what is commit object.
A commit object contains :
  - reference to commit objects and tree objects.
  - reference to blob objects.
  - commit message.
  - also stores pointer to its parent(s) commit(s).

#### About parent commits
  1. 0 parent = initial commit
  2. 1 parent = usual commit
  3. multiple parents = commit resulting from merging 2 or more branches
---------------------------------------------------------------------------------------

## What happens when we stage a file?
Let's see what happens at the staging time:
  - computes the checksum for each file
  - stores a version of file in a git repo(blob)
  - adds checksum into staging area
----------------------------------------------------------------------------------------

## What happens when we commit a file?
When you make a commit, git stores a commit object that contains a pointer to the snapshot of the content you staged.
Following happens upon committing a file:
  - checksums each subdirectory
  - stores it as a tree object in git repo
--------------------------------------------------------------
## What is this commit, tree and blob?
  1. **commit** : The files which are present in the staging area and needs to be committed. It has some size, some SHA-1 hash ID of tree, author and committer, and is the first commit of the project pointing towards something called tree.

  2. **tree** : A Git tree object creates the hierarchy between files in a Git repository. You can use the Git tree object to create the relationship between directories and the files they contain. These endpoints allow you to read and write tree objects to your Git database on GitHub. We can again see size and some blobs and their SHA-1 hash ID and their names pointing towards multiple blobs.

  3. **blob** : A Git blob(binary large object) is the object type used to store the contents of each file in a repository. The file's SHA-1 hash is computed and stored in the blob object.
---

## Branches 

Git branches are effectively a pointer to a snapshot of your changes. When you want to add a new feature or fix a bug(no matter how big or small) you spawn a new branch to encapsulate your changes. Branches are cheap and easy to merge. Switching back and forth the branches is also very easy.
#### Some commands related to branches
- `git branch` : list all branches in your repository
- `git branch <branch>` : create a new branch called ＜branch＞. This does not check out the new branch.
- `git checkout <branch>` : lets you navigate between the branches created by git branch 
- `git switch <branch>` : allows you to switch your current HEAD branch
- `git branch -d <branch>` : Delete the specified branch. This is a “safe” operation in that Git prevents you from deleting the branch if it has unmerged changes
- `git branch -D <branch>` : Force delete the specified branch, even if it has unmerged changes. This is the command to use if you want to permanently throw away all of the commits associated with a particular line of development
- `git branch -m <branch>` : rename the current branch to "branch"
- `git branch -a` : list all the remote branches

>HEAD : it points out the last commit in the current checkout branch. It is like a pointer to any reference. The HEAD can be understood as the "current branch." When you switch branches with 'checkout,' the HEAD is transferred to the new branch.


