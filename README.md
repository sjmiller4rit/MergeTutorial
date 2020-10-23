# Merge Tutorial

### Objective
Resolve a Merge Conflict

### Repository Details
In the master branch there are two files:
- This README.md file
- example.txt 

In branch1, the only difference is that example.txt is modified with the name "John Smith"



### Steps:
<ol>
  
  <li>
<details>
  <summary>Fork this Repository</summary>
<br /> <img src="https://i.ibb.co/kQ242r6/Screen-Shot-2020-10-23-at-1-43-09-PM.png" alt="forkRepo" />
Now go to your profile and copy the url to your forked repository.
</details>
  </li>
  
  <li>
<details>
  <summary>Clone your Forked Repository</summary> 

Create a directory, `cd` into it, then clone your ***Forked repository*** (NOT THE MAIN ONE) and `cd` into that. Do a `dir` (windows) or `ls` (mac, bash, linux) and make sure you see both files listed (example.txt and README.md). <br />
If you don't see the files, you're most likley in the wrong directory! You can use `pwd` to check your current path
</details>
  </li> 
   <li>
<details>
  <summary>Create a Branch</summary>
  
Remember to use proper naming conventions! <br />
You can either use `git branch <NAME OF BRANCH>` or `git checkout -b <NAME OF BRANCH>` <br />
If you use the first one, you'll also have to checkout with `git checkout <NAME OF BRANCH>` <br />
You can check what branch you're on by doing a `git branch`
</details>
  </li>
  <li>
<details>
  <summary>Modify example.txt</summary>
  
Modify example.txt by opening the file in a text editor or through the command line (nano, vim etc). Add your name after the arrow.
</details>
  </li>
    <li>
<details>
  <summary>Stage your Changes</summary>
  
Once you have saved your file, stage your work / file with any of the following commands:
<ul>
  
  <li>
  
  `git add .`
</li>
  <li>
  
  `git add -a` or `git add -A`</li>
  <li>
  
  `git add <FILE NAME>`</li>  
</ul>
 If you would like, you can check the status of your workflow and changes with `git status` before and after you stage your work.  
</details>
  </li>
    <li>
<details>
  <summary>Commit this Stage</summary>
  
`git commit -m "YOUR MESSAGE HERE"`
Make sure you use proper message conventions!
</details>
  </li>
   <li>
<details>
  <summary>Push this Commit</summary>
  
Since this is a new branch you may have to `set--upstream`.Try to `git push` and see if it's successful, otherwise follow the directions in the output.
</details>
  </li>
  <li>
<details>
  <summary>Merge your Branches</summary>
  
Switch to branch1 with `git checkout branch1`, then merge the branch you created using `git merge <yourBranchName>` You should see a merge conflict alert like so.
<br /> <img src="https://i.ibb.co/DbbwPt7/Screen-Shot-2020-10-23-at-1-14-35-PM.png" alt="mergeConflict" />
</details>
  </li>
  <li>
<details>
  <summary>Explore the Branches and Files</summary>
  
Take a moment to read through the output and re-open the file. What does it look like? You should see something like this:
<br /> <img src="https://i.ibb.co/RbJs9Yg/Screen-Shot-2020-10-23-at-1-16-58-PM.png" alt="mergeConflictOutput" />
</details>
  </li>
  <li>
<details>
  <summary>Resolve Merge Conflict Manually</summary>
  
Fix the merge conflict manually by removing the "John Smith" line and keeping yours. Once again, this can be done through a text editor or through the command line.
<br /> <img src="https://i.ibb.co/d0dtFTM/Screen-Shot-2020-10-23-at-1-17-23-PM.png" alt="fixedMergeConflict" />
</details>
  </li>
  <li>
<details>
  <summary>Push your Changes</summary>
  
Now that you have (or at least you think you have) resolved the merge conflict, let's try adding, commiting and pushing the commit. If everything works, then you have successfully fixed the merge conflict! 
</details>
  </li>
</ol>


### When you are done:
Delete your outdated branch either through GitHub's interface or through the Command Line:
1. Make sure you are on a different branch than the one you are trying to delete
2. Delete the brach locally: 
<br />  `git branch -d <localBranchName>`
3. Finally, make sure this change is made remotely (if you want to delete it for everyone)
<br /> `git push origin --delete <remoteBranchName>`
