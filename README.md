## Merge Tutorial

### Objective
Resolve a Merge Conflict

### Repository Details
In the master branch there are two files:
- This README.md file
- example.txt 

In branch1 the only difference is that example.txt is modified with the name "John Smith"



### Steps:
1. Fork this Repository.
2. Create a directory, `cd` into it, then clone your ***Forked repository*** and `cd` into that. Do a `dir` or `ls` to make sure you see both files (example.txt and README.md)
3. Create a branch then checkout. Make sure you're on the proper branch by doing a `git branch`.
4. Modify example.txt by opening the file in a text editor or through the command line. Add your name after the arrow.
5. Once you have saved your file, do a `git status`, then stage your file.
6. Commit this stage (with proper message conventions!)
7. Push this commit. Since this is a new branch you may have to `set--upstream`
8. Switch / checkout to branch1, then merge your branch into it with `git merge <branchName>` You should see a merge conflict alert like so.
<br /> <img src="https://i.ibb.co/DbbwPt7/Screen-Shot-2020-10-23-at-1-14-35-PM.png" alt="mergeConflict" />
9. Take a moment to read through the output and re-open the file. What does it look like?
<br /> <img src="https://i.ibb.co/RbJs9Yg/Screen-Shot-2020-10-23-at-1-16-58-PM.png" alt="mergeConflictOutput" />
10. Fix the merge conflict manually by removing the "John Smith" line and keeping yours. Once again, this can be done through a text editor or through the command line.
<br /> <img src="https://i.ibb.co/d0dtFTM/Screen-Shot-2020-10-23-at-1-17-23-PM.png" alt="fixedMergeConflict" />
11. Now that you have (or at least you think you have) resolved the merge conflict, let's try adding, commiting and pushing the commit. If everything works, then you have successfully fixed the merge conflict! 



### When you are done:
Delete your outdated branch either through GitHub's interface or through the Command Line:
1. Make sure you are on a different branch than the one you are trying to delete
2. Delete the brach locally: 
<br />  `git branch -d <localBranchName>`
3. Finally, make sure this changeis made remotely (if you want to delete it for everyone)
<br /> `git push origin --delete <remoteBranchName>`
