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
   - call "git status"; these have not been added to the index before it can be committed
   - call "git add %filename%"
