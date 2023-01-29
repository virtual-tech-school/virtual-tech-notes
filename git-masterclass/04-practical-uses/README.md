Contribute notes based on [this](https://www.youtube.com/watch?v=jp_fOkie4gs&list=PL2kSRH_DmWVajYgFoP-HVKK5VKkzFYyzp&index=4) video now!

# CONTENT:
- [COMMIT HISTORY](#commit-history) 
- [CREATING A NEW BRANCH & COMMITTING CHANGES](#CREATING-A-NEW-BRANCH-&-COMMITTING-CHANGES)
- [MERGING BRANCHES](#MERGING-BRANCHES)
  - ["FAST-FORWARD" MERGING]("FAST-FORWARD"-MERGING)
  - ["3 WAY" MERGING]("3-WAY"-MERGING)
- [RESOLVE MERGE CONFLICTS](#RESOLVE-MERGE-CONFLICTS)
- [BRANCH MANAGEMENT COMMANDS](#BRANCH-MANAGEMENT-COMMANDS)
- [DELETE A BRANCH THAT IS NOT MERGED](#DELETE-A-BRANCH-THAT-IS-NOT-MERGED)
- [COMMIT HISTORY](#COMMIT-HISTORY)
- [NOTE](#NOTE)
## COMMIT HISTORY:
*starting with some commits in the **main** branch.* 
## CREATING A NEW BRANCH & COMMITTING CHANGES:
### CREATING "01-INTRODUCTION" BRANCH:
```sh
	//create a new branch "01-introduction",
	 git branch 01-introduction
	//switch HEAD from "main" branch to "01-introduction",
	 git checkout 01-introduction
	
	 //done with changes to "01-introduction", now commit the changes.
	 
	 // to stage the changes,
	 git add .
	 // commit changes.
	 git commit -m "commit on 01-introduction"
```
```sh
Switch to main branch:
	 git switch main
```

### CREATING "02-BASIC-COMMANDS" BRANCH:
```sh
Create "02-basic-commands":
	 
	// create a new branch "02-basic-commands",
	 git branch 02-basic-commands
	 
	//switch HEAD from main branch to "Branch2",
	 git checkout 02-basic-commands
	
	 //done with changes to "02-basic-commands", now commit the changes.
	 
	 // to stage the changes,
	 git add .
	 // commit changes.
	 git commit -m "commit on Branch2"
```

```sh
Switch to main branch:
	 git switch main
```

**Now we have 2 new branches diverging from the main branch, 
And the git HEAD will be pointing to main.** 

## MERGING BRANCHES:
### "FAST FORWARD" MERGING:
```sh
-As we are in "main" branch,
-if we merge the "01-introduction" with the current branch,
  //git merge 01-introduction
-then the "main" branch pointer points to the commit that "01-introduction" branch is pointing to.
-This is also called as "Fast-Forward".

// delete "01-introduction" branch.
git branch -d 01-introduction
```
### "3 WAY" MERGING:
```sh
- If we merge the "02-basic-commands" with "main" branch , 
  // git merge 02-basic-commands
- As these two branches are diverged (commits these branches are pointing are not direct ancestors) ,
- 3 way merge takes place, also called "merge made by the 'ort' strategy",
- git will create a new commit by taking the snapshot from the commits of two branches.
- The main branch points to the new commit.
- Now we can delete the "02-basic-commands" branch, as it is merged with the "main" branch.

// delete "02-basic-commands" branch.
 git branch -d 02-basic-commands
```


## RESOLVE MERGE CONFLICTS:
- While doing **3 way merges** , we may encounter conflict that the two commits may have different data in the same lines from some files.
- Git cannot decide on what data has to be taken for the new commit.
- In that case we have to remove the conflict data , and manual commit the changes.

## BRANCH MANAGEMENT COMMANDS:
    git branch 
    - will show all the branches.
    git branch -v
    - will show all the branches with the last commit message.
    git branch --merged 
    - will show the branches that are merged with the current branch.


## DELETE A BRANCH THAT IS MERGED:
	git branch -d BranchName
## DELETE A BRANCH THAT IS NOT MERGED:
    git branch -D BranchName
    
## COMMIT HISTORY:
    
    git log  
    - all the commits with author details, time and check-sum.
    git log --stat  
    - git logs along with files that are modified in that commit.
    git log --pretty=oneline  
    - presents each commit details in a single line.

# NOTE: 
	1) When we are switching to new branch,
	    there should be no pending changes in the working tree of present branch, 
	    otherwise git will not allow us to switch.
    2) But in-case , 
        if we don’t want to commit changes in the current branch for now, 
        but want to switch to other branch, we can store the changes temporarily using stash.


