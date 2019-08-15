# Adding large files to gituhb

`git lfs install`

### to add a file type that you would liek to track, you add *.<fileType>

`git lfs trace "*.th" ` 

`git add .gitattributes `


### Then add / commit  files as usual. 


# Removing accidentally added large files before 

### if anythign goes wrong with the following approach, type:
`git rebase --abort`
### if you have not pushed just use:

`git reset --head soft `

### If you have pushed

`git log --all -- <name_of_large_file_accidentally_commit_and_pushed>`

### go to the  bottom (last commit in the index) 

### Assuming commit number 3f7dd04a6e6dbdf1fff92df1f6344a06119d5d32

`git rebase -i 3f7dd04a6e6dbdf1fff92df1f6344a06119d5d32`

### there may be commits that you need to replace. 

## Alternative method


### *Note*: This command changes the hashes of your commits which can be a real problem, especially on shared repositories. It should not be performed without understanding the consequences.

git filter-branch --index-filter 'git rm -r --cached --ignore-unmatch <file/dir>' -f HEAD 