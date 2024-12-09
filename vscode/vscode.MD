#### Project settings
`.vscode/settings.json`

#### Global settings file
Windows: `%APPDATA%\Code\User\settings.json`  
Linux: `~/.config/Code/User/settings.json`

#### Debug configuration
`launch.json`

#### Debug with venv:
`Ctrl + Shift + P` → Select venv in: `Python: Select Interpreter`

#### Debug pytest
`.vscode/launch.json`:
```
{
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Run pytest",
            "type": "debugpy",
            "request": "launch",
            "module": "pytest",
            "console": "integratedTerminal",
            "args": ["-v", "-s"],
            "cwd": "${workspaceFolder}"
        }
    ]
}
```