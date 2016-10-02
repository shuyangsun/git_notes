
git init
	Initialize a repo.

git status
	Check the status of a repo, this is for snapshots.

git log
	Check all the stagings, this is for commits.
	--oneline: Log all commits history with oneline description.
	[filename]: Log commits history only for given files.

git add
	Add changed files into current snapshot (staging). Once it's snapshoted, "git commit" will commit it as it is RIGHT NOW.

git commit
	Commit current stage, with auto opened text editor for commit messages.
	-m "Commit Message": Commit with message inline instead of opening text editor.

git checkout [commitID]
	Checkout a specific commit, working copy will become identical to that commit.

git tag -a [tagID] -m "Message"
	Tag current commit with a tagID (shortcut to this commitID, normally version number like v1.0), and a message.
	The -a flag is to create an annotated tag, which let's us record our name, the date, and a descriptive message.

git tag
	Shows all the tags.

git revert [commitID]
	Undo changes in "commitID".
	The undo-ed commit is still accessible, git is designed to NEVER lose history.

git reset
	Unstage all staged files (undo all "git add [fileName]").
	--hard: Reset all tracked files to original state of the last commit.

git clean -f
	Remove all untracked files.

HEAD is Git's internal way of indicating the snapshot that is currently checked out.

git branch
	List all branches
	[branchName]: Create a new branch, but does NOT check it out. Use "git checkout [branchName]" to checkout that branch.

git merge [branchName]
	Merge given branch to current branch.

git branch -d [branchName]
	Delete given branch if fully merged.

git rm [fileName]
	Remove file and stop tracking it.
	--cached: Keep the file.
	-f: Force removal.
