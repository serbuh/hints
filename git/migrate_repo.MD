### To migrate the repo from A to B

1. Clone A locally in mirror mode
```
git clone --mirror <url-of-A>
cd <name-of-cloned-folder>.git
```
This creates a bare mirror repo with all branches, tags, remotes, etc.

2. Push everything to A_mirror
```
git remote set-url --push origin <url-of-A_mirror>
git push --mirror
```


### To update submodule link

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