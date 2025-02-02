Install (linux)
```
sudo snap install astral-uv
```

Install (Windows)
```
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

Create new project
```
cd project
uv init
uv add numpy
uv run app.py
```