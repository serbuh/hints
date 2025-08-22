C | A
-|-
ctrl + A | Home
ctrl + E | End

C | A
-|-
set -e | exit immediately if any command fails
set -u | treat unset variables as an error.
set -o pipefail | a pipeline fails if any command in it fails (not just the last one)

```
set -x # start trace (print the command before execution)
CMD
set +x # stop trace
```
