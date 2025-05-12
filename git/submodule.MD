### Change submodule url

1. Update URL in .gitmodules (used for clone/init)
```
git config -f .gitmodules submodule.A_sub.url git@github.com:mirror/sub.git
```

Or manually edit .gitmodules:
```
[submodule "A_sub"]
  path = A_sub
  url = git@myserver.com:mirror/sub.git
```

2. Update the actual submodule's remote
```
git -C <path-to-submodule> remote set-url origin git@myserver.com:mirror/lib.git
```
This ensures that future `git submodule update --remote` or `git fetch` in the submodule uses the mirror.

3. Verify
`git -C A_sub remote -v` - check submodule's remote


### Updating the submodule according to the commit (including a url change)
```
git submodule sync
git submodule update --init --recursive
```
### Explanation
```
git submodule sync
```
Updates the local `.git/config` with the remote URL from .gitmodules (which is now the old one again from the checked-out commit).
```
git submodule update --init --recursive
```
Initializes the submodule, checks out the correct commit, and uses the URL now listed in .gitmodules.
