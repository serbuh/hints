# Config
vscode global settings:
`%APPDATA%\Code\User\settings.json`
```
    "pylint.args": [
        "--disable=line-too-long",
        "--disable=invalid-name",
        "--disable=missing-function-docstring",
        "--disable=relative-beyond-top-level",
        "--disable=missing-class-docstring",
        "--disable=trailing-whitespace",
        "--disable=missing-module-docstring",
        "--init-hook=import os;os.chdir(\\\"/home/sergeybu/FW/fw_cvas\\\")"
    ],
```