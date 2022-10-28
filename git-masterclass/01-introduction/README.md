Contribute notes based on [this](https://www.youtube.com/watch?v=LQ2LTPHeTts&list=PL2kSRH_DmWVajYgFoP-HVKK5VKkzFYyzp&index=1) video now!



# Contents

- [01 What is Git ?](#01-what-is-git)

- [02 Version Control System (VCS)](#02-version-control-system-vcs)
- [03 Types of Version Control System (VCS)](#03-types-of-version-control-system-vcs)
  - [Local Version Control System](#1-local-version-control-system)
  - [Centralized Version Control System](#2-centralized-version-control-system)
  - [Distributed Version Control System](#3-distributed-version-control-system)
- [04 How was Git created ?](#04-how-was-git-created)
- [05 How Git is different from other Version Control System ?](#05-how-git-is-different-from-other-version-control-system)
  - [Snapshorts, Not Differences](#1-snapshorts-not-differences)
  - [Nearly Every Operation Is Local](#2-nearly-every-operation-is-local)
  - [Git Has Integrity](#3-git-has-integrity)
  - [Git Generally Only Adds Data](#4-git-generally-only-adds-data)

# 01 What is Git ?

Git is a **Version Control System (VCS)** for your files

- It reverts a selected file/entire project back to previous state
- Compares changes
- Helps in indentification of who modified the files that is causing some issue
- Helps in identification of who introduced an issue and when

# 02 Version Control System (VCS)

- Version control, also known as source control, is the practice of tracking and managing changes to software code.
- Version control systems are software tools that help software teams manage changes to source code over time.
- Version control software keeps track of every modification to the code in a special kind of database.
- If a mistake is made, developers can turn back the clock and compare earlier versions of the code to help fix the mistake while minimizing disruption.

# 03 Types of Version Control System (VCS)

### 1. Local Version Control System

- Contains the Version Database located on your computer.
- Every file change is stored as a patch.
- Every patch set contains only the changes made to the file since its last version.

#### Problems:-

- Since , stored locally collaboration with other developer or a team is not possible.
- If anything happens to local database , all the patches would be lost.
- If anything happens to single version , alll the changess made after that version would be lost.

### 2. Centralized Version Control System

- Contains a single server that contains all the file versions.
- Allows multiple clients to simultaneously access files on the server.
- Allows to pull files to their local computer or push onto server from their local computer.
- Administrators have control over who can do what and what not.
- Allows for easy collaboration with other developer or a team.

#### Problems:-

- Single point of failure.
- As everything is stored on the centralized server. If something were to happen to that server, nobody can save their versioned changes, pull files or collaborate at all.
- If the central database became corrupted, and backups haven't been kept, you lose the entire history of the project except whatever single snapshots people happen to have on their local machines.

### 3. Distributed Version Control System

- Clients don’t just check out the latest snapshot of the files from the server, they fully mirror the repository, including its full history.
- Everyone collaborating on a project owns a local copy of the whole project, i.e. owns their own local database with their own complete history.
- If the server becomes unavailable or dies, any of the client repositories can send a copy of the project's version to any other client or back onto the server when it becomes available.
- It is enough that one client contains a correct copy which can then easily be further distributed.

#### Example :-

Git is the most well-known example of Distributed Version Control System (DVC sys).

# 04 How was Git created ?

As with many great things in life, Git began with a bit of creative destruction and fiery controversy.

The Linux kernel is an open source software project of fairly large scope. During the early years of the Linux kernel maintenance (1991–2002), changes to the software were passed around as patches and archived files. In 2002, the Linux kernel project began using a proprietary DVCS called BitKeeper.

In 2005, the relationship between the community that developed the Linux kernel and the commercial company that developed BitKeeper broke down, and the tool’s free-of-charge status was revoked. This prompted the Linux development community (and in particular Linus Torvalds, the creator of Linux) to develop their own tool based on some of the lessons they learned while using BitKeeper. Some of the goals of the new system were as follows:

- Speed
- Simple design
- Strong support for non-linear development (thousands of parallel branches)
- Fully distributed
- Able to handle large projects like the Linux kernel efficiently (speed and data size)

Since its birth in 2005, Git has evolved and matured to be easy to use and yet retain these initial qualities. It’s amazingly fast, it’s very efficient with large projects, and it has an incredible branching system for non-linear development

# 05 How Git is different from other Version Control System ?

## 1. Snapshots, not Differences

- #### Others:

  - Most other systems store information as a list of file-based changes. These other systems think of the information they store as a set of files and the changes made to each file over time.

- #### Git:
  - Git thinks of its data more like a series of snapshots of a miniature filesystem
  - With Git, every time you commit, or save the state of your project, Git basically takes a picture of what all your files look like at that moment and stores a reference to that snapshot
  - To be efficient, if files have not changed, Git doesn’t store the file again, just a link to the previous identical file it has already stored. Git thinks about its data more like a **stream of snapshots**.

## 2. Nearly Every Operation Is Local

- Most operations in Git need only local files and resources to operate — generally no information is needed from another computer on your network
- You have the entire history of the project right there on your local disk, most operations seem almost instantaneous

#### Example:-

To browse the history of the project, Git doesn’t need to go out to the server to get the history and display it for you — it simply reads it directly from your local database. This means you see the project history almost instantly. If you want to see the changes introduced between the current version of a file and the file a month ago, Git can look up the file a month ago and do a local difference calculation, instead of having to either ask a remote server to do it or pull an older version of the file from the remote server to do it locally.

## 3. Git Has Integrity

- Everything in Git is checksummed before it is stored and is then referred to by that checksum.
- This means it’s impossible to change the contents of any file or directory without Git knowing about it.
- The mechanism that Git uses for this checksumming is called a SHA-1 hash.
- This is a 40-character string composed of hexadecimal characters (0–9 and a–f) and calculated based on the contents of a file or directory structure in Git.
- A SHA-1 hash looks something like this:

```
24b9da6552252987aa493b52f8696cd6d3b00373
```

## 4. Git Generally Only Adds Data

- When you do actions in Git, nearly all of them only _add_ data to the Git database.
- It is hard to get the system to do anything that is not undoable or to make it erase data in any way.
- After you commit a snapshot into Git, it is very difficult to lose, especially if you regularly push your database to another repository.
