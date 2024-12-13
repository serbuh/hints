C | A
-|-
sudo apt install pre-commit | Install
pre-commit --version | Verify
.pre-commit-config.yaml | Create yaml in the repo folder
pre-commit autoupdate | update the hooks to the latest versions
pre-commit install | Install the pre-commit hooks
pre-commit run --all-files | run pre-commit manually
git commit --no-verify | Commit bypassing pre-commit hook

Example yaml:
```
repos:
  - repo: https://github.com/pre-commit/pre-commit-hooks
    rev: v4.4.0
    hooks:
      - id: trailing-whitespace
      - id: end-of-file-fixer
      - id: check-yaml
      - id: check-added-large-files

  - repo: https://github.com/psf/black
    rev: 23.3.0
    hooks:
      - id: black
        language_version: python3

  - repo: https://github.com/PyCQA/isort
    rev: 5.12.0
    hooks:
      - id: isort
        args: ["--profile", "black"]
```
