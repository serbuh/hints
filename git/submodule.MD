# General commands
### Submodules
C | A
-|-
`git submodule update --remote` | Pull the latest commit in the submodule
`git submodule update --init --recursive` | Initialize the submodule, checks out the correct commit
`git submodule foreach --recursive 'git reset --hard'` | Run command in all submodules


# Change submodule's url
```
git config -f .gitmodules submodule.<path-to-submodule>.url <new-git-url>
git -C <path-to-submodule> remote set-url origin <new-git-url>
```
### Explanation
1) Update URL in .gitmodules (used for clone/init):  
`git config -f .gitmodules submodule.<path-to-submodule>.url <new-git-url>`  
Or manually edit .gitmodules:
```
[submodule "A_sub"]
  path = A_sub
  url = git@myserver.com:mirror/sub.git
```

2) Update the actual submodule's remote:  
`git -C <path-to-submodule> remote set-url origin <new-git-url>`  
(This ensures that future `git submodule update --remote` or `git fetch` in the submodule uses the mirror)

3) Verify new urls  
`git -C A_sub remote -v` - check submodule's remote

# Updating the submodules according to the commit (including a url change)
```
git submodule sync
git submodule update --init --recursive
```
### Explanation
1) Update the local `.git/config` with the remote URL from .gitmodules (which is now the old one again from the checked-out commit):  
`git submodule sync`
2) Initialize the submodule, checks out the correct commit, and uses the URL now listed in .gitmodules.  
`git submodule update --init --recursive`
