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