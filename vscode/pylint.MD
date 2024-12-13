# Config
vscode global settings:
`%APPDATA%\Code\User\settings.json`

or  

`Ctrl + Shift + P` -> `Open User Settings (JSON)` -> Add:
```
    "pylint.args": [
        "--disable=line-too-long",
        "--disable=invalid-name",
        "--disable=missing-function-docstring",
        "--disable=relative-beyond-top-level",
        "--disable=missing-class-docstring",
        "--disable=trailing-whitespace",
        "--disable=missing-module-docstring",
        "--disable=broad-exception-raised",
        "--init-hook=import os;os.chdir(\\\"/home/sergey/Workspace/my_proj\\\")"
    ],
```