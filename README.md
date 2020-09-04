# pre-commit
Pre-commit custom hooks
* id: [python-black](https://github.com/psf/black) # Python opinionated code formatter
* id: [python-flake8](https://flake8.pycqa.org/en/latest/) # Python flake8 style enforcement
* id: [python-bandit](https://pypi.org/project/bandit/) # Python security linter / SAST
# Usage
## Dependencies
```$ pip3 install --user pre-commit```
### Optional dependencies
```$ pip3 install --user black```
```$ pip3 install --user flake8```
```$ pip3 install --user bandit```

## Example Repo Config
```
$ cat .pre-commit-config.yaml 
repos:
-   repo: https://github.com/pre-commit/pre-commit-hooks
    rev: v3.2.0
    hooks:
    -   id: trailing-whitespace
    -   id: end-of-file-fixer
    -   id: check-yaml
    -   id: check-added-large-files
    -   id: detect-aws-credentials
    -   id: detect-private-key
-   repo: git@github.com:commit-bneyedli/pre-commit-hooks.git
    rev: bda7163e859a4c3a7a72f4e63c550481e58f04c9
    hooks:
    -   id: python-black
    -   id: python-flake8
    -   id: python-bandit
```
## Repo init
```
$ pre-commit autoupdate
Updating https://github.com/pre-commit/pre-commit-hooks ... already up to date.
Updating git@github.com:commit-bneyedli/pre-commit-hooks.git ... [INFO] Initializing environment for git@github.com:commit-bneyedli/pre-commit-hooks.git.
$ pre-commit install
pre-commit installed at .git/hooks/pre-commit
```
