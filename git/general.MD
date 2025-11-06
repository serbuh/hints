C | A
-|-
`git -C <path> <command>` | Pretend you're in the <path> directory when running this command.
`git branch -vv` | Check upstreams for each branch
`git branch -f branch_name HEAD` | Reset oother branch (branch_name) to the HEAD
`git checkout <commit> -- <file>` | Reset file to revision from other commit
`git show <commit>` | Show diff of specific commit
`git branch -D branch_name` | Delete local branch
`git push origin :branch_name` | Delete remote branch (old style)
`git push origin --delete branch_name` | Delete remote branch (new style)