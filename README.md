# git-github
Tutorial on how to make an create, push and pull an example repository.
For more details: https://www.youtube.com/watch?v=xuB1Id2Wxak
1. Create a repository
  to create a repository 
  - press create repository in github ( make sure to create a readme file )
  - create a folder on your local computer for the new repository
  - within the local folder, you can right click and open terminal (gitbash)
  - within terminal call "git init"; there should be a new .git file in the folder
2. Sync the repository
  syncing the local repository in the folder with the central repository created in github
   - From the github central repository screen copy to the clipboard the URL 
   - in the terminal call "git remote add origin "%paste the URL from the github website here%"
   Check if syncing worked correctly by pulling from the central repository
   - call "git pull"; within you local repository folder there should be your ReadMe file from central
3. Make Changes
   the midstep in the local git is called an Index. After a file (text file or piece of code)  is created in your synced local repository before it is committed back to the local or central repository it is held in this index. To see what files you have that are new but have not added to the index to be committed.
   - call "git status"; the files in red have not been added to the index before it can be committed
   - call "git add %filename%" or if there are multiple new files in red or modified files call "git add -A"; now all of these are added to the index and can be committed
   - check if they have been added to the index with "git status";  if they are green they were all indexed
   Commit 
   - to commit all the files call "git commit -a -m "adding 3 files together"; "-m" must be in commmand line (if message window opens press i for insert, type message, press esc, enter :x!, hit enter) when committing pushing or pulling; if you have already indexed the file once you don't have to reindex and commit when something has been modified you can just "git commit -a -m" for the rest of the time 


4. Parallel Development and Branching
   How  to create different branches (allows you to duplicate a git folder and files from the master and work on them without disrupting the original files)
   - call "git branch %branchname%"; creates the branch
   - call "git checkout %branchname%"; switches into whatever branch name you call that you have created
   Files can now be added (from your local repo library) using "git add %filename%
   - call "ls"; shows a list of all the filenames in the branch you are in; if you "git checkout master" and "ls" they will not have any of the new files you have added to the other branch
   if there is a feature that you are working on that you would like to pause and not commit to your master or branch codes you can call "git stash" to stash it away until you would like to add it back to the branch or master
    
   How to merge the new file back to your master branch (production quality code)
    - call "git merge %branchname%"
    
   "git pull" = "git fetch" + "git merge"
   
   How to rebase - which cleans up all of the commit history 
   -  git rebase %branchname to merge into master%
  
      
   
   
   
