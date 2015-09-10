Title: Untracking and removing already pushed files in Git
Date: 2015-09-08 13:01
Tags: Programming, Command

I had the problem of wanting to remove and ignore files that I have already commit-ed to git. Turns out, it's pretty simple:

1. Add the files you want to ignore to your *.gitignore* file  
2. To unstage and remove paths only from the index, not the file system, run:  
`git rm -r --cached .`
3. Run:  
`git add .`
4. Run:  
`git commit -m "Removed sensitive files"`

The files/paths listed in *.gitignore* should now be gone from the repository but should still exist in your file system.

Note: This will not remove files already pushed to your git repository. To remove sensitive data already pushed, see [this article](https://help.github.com/articles/remove-sensitive-data/)

