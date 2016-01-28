# git-prune

Tool to remove git repository history for all branches before specific commit, recreate master and filter obsolete branches by checking for reference commit.

## Usage

```
cd /path/to/git/project
git-prune -g=starting_commit_hash [ -o=reference_commit_hash ] [ -m=new_master_branch ] [ -c ]
	-g - commit hash to remove history before
	-o - commit hash to check branches against
	-m - name of the branch to create new master from
	-c - perform aggressive garbage collection
```

## Notes

When no reference commit specified with -o, all branches not containing starting commit will be considered obsolete.
