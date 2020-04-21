---
layout: post
title:  "Git Cheat Sheet"
author: nikhil
categories: [ GitHub, Git ]
image: assets/images/git/cheatsheet.png
tags: [github,git,cheat sheet]
---

Git is the free and open source distributed version control system that's responsible for everything GitHub
related that happens locally on your computer. This cheat sheet features the most important and commonly
used Git commands for easy reference.

### INSTALLATION & GUIS  
With platform specific installers for Git, GitHub also provides the ease of staying up-to-date with the latest
releases of the command line tool while providing a graphical user interface for day-to-day interaction, review, and 
repository synchronization.

### Git for All Platforms  
  <a href="https://git-scm.com/downloads" target="_blank">https://git-scm.com/downloads</a>

## SETUP  
Configuring user information used across all local repositories.  
**git config --global user.name “[firstname lastname]”** &#8212;
set a name that is identifiable for credit when review version history  
**git config --global user.email “[valid-email]”** &#8212;
set an email address that will be associated with each history marker  
**git config --global color.ui auto** &#8212;
set automatic command line coloring for Git for easy reviewing  

## SETUP & INIT   
Configuring user information, initializing and cloning repositories.  
**git init** &#8212;
initialize an existing directory as a Git repository  
**git clone [url]** &#8212;
retrieve an entire repository from a hosted location via URL  

## STAGE & SNAPSHOT  
Working with snapshots and the Git staging area.  
**git status** &#8212;
show modified files in working directory, staged for your next commit  
**git add [file]** &#8212;
add a file as it looks now to your next commit (stage)  
**git reset [file]** &#8212;
unstage a file while retaining the changes in working directory  
**git diff** &#8212;
diff of what is changed but not staged  
**git diff --staged** &#8212;
diff of what is staged but not yet commited  
**git commit -m “[descriptive message]”** &#8212;
commit your staged content as a new commit snapshot  

## BRANCH & MERGE  
Isolating work in branches, changing context, and integrating changes.  
**git branch** &#8212;
list your branches. a * will appear next to the currently active branch  
**git branch [branch-name]** &#8212;
create a new branch at the current commit  
**git checkout** &#8212;
switch to another branch and check it out into your working directory  
**git merge [branch]** &#8212;
merge the specified branch’s history into the current one  
**git log** &#8212;
show all commits in the current branch’s history  

## INSPECT & COMPARE  
Examining logs, diffs and object information  
**git log** &#8212;
show the commit history for the currently active branch  
**git log branchB..branchA** &#8212;
show the commits on branchA that are not on branchB  
**git log --follow [file]** &#8212;
show the commits that changed file, even across renames  
**git diff branchB...branchA** &#8212;
show the diff of what is in branchA that is not in branchB  
**git show [SHA]** &#8212;
show any object in Git in human-readable format  

## TRACKING PATH CHANGES  
Versioning file removes and path changes.  
**git rm [file]** &#8212;
delete the file from project and stage the removal for commit  
**git mv [existing-path] [new-path]** &#8212;
change an existing file path and stage the move  
**git log --stat -M** &#8212;
show all commit logs with indication of any paths that moved  

## IGNORING PATTERNS  
Preventing unintentional staging or commiting of files  
<b>logs/  
*.notes  
pattern*/</b>  

Save a file with desired paterns as .gitignore with either direct string matches or wildcard globs.  
**git config --global core.excludesfile [file]** &#8212;
system wide ignore patern for all local repositories  

## SHARE & UPDATE  
Retrieving updates from another repository and updating local repos  
**git remote add [alias] [url]** &#8212;
add a git URL as an alias  
**git fetch [alias]** &#8212;
fetch down all the branches from that Git remote  
**git merge [alias]/[branch]** &#8212;
merge a remote branch into your current branch to bring it up to date  
**git push [alias] [branch]** &#8212;
Transmit local branch commits to the remote repository branch  
**git pull** &#8212;
fetch and merge any commits from the tracking remote branch  

## REWRITE HISTORY  
Rewriting branches, updating commits and clearing history  
**git rebase [branch]** &#8212;
apply any commits of current branch ahead of specified one  
**git reset --hard [commit]** &#8212;
clear staging area, rewrite working tree from specified commit  

## TEMPORARY COMMITS   
Temporarily store modified, tracked files in order to change branches.  
**git stash** &#8212;
Save modified and staged changes  
**git stash list** &#8212;
list stack-order of stashed file changes  
**git stash pop** &#8212;
write working from top of stash stack  
**git stash drop** &#8212;
discard the changes from top of stash stack  

Download the pdf version of GitHub Cheat Sheet provided by GitHub Education <a href="https://education.github.com/git-cheat-sheet-education.pdf" target="_blank" title="GitHub Cheat Sheet pdf">here</a>.

### GitHub Desktop  
  To download GitHub Desktop on to your personal devices, visit GitHub Desktop site <a href="https://desktop.github.com/"         target="_blank" title="GitHub Desktop">here</a>.

  For Linux and Solaris platforms, the latest release is available on the official Git web site.
