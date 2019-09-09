
# Adding large files to gituhb
Before commiting the large file, first install git-lfs in the repository where the big file you want to commit exists.
`git lfs install`

then to add a file type that you would like to track, you add *.<fileType>, here we are adding files with extension `.th`

`git lfs trace "*.th" ` 

`git add .gitattributes `

Once completed, add and then commit  the file/s as usual. 


# Removing accidentally commited large files 

If anything goes wrong with the following approach (below), type:
`git rebase --abort`

If you have not pushed just use:

`git reset --head soft `

If you have pushed

`git log --all -- <name_of_large_file_accidentally_commit_and_pushed>`

go to the  bottom (last commit in the index) 

assuming commit number 3f7dd04a6e6dbdf1fff92df1f6344a06119d5d32

`git rebase -i 3f7dd04a6e6dbdf1fff92df1f6344a06119d5d32`

there may be commits that you need to replace. 

## Alternative method

#### *Note*: This command changes the hashes of your commits which can be a real problem, especially on shared repositories. It should not be performed without understanding the consequences.

`git filter-branch --index-filter 'git rm -r --cached --ignore-unmatch <file/dir>' -f HEAD `
