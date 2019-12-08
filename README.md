# Pipenv cheatsheet

## Installation

`pip install pipenv`

## Installation Commands

| Commands         | Description | 
|:-----------------|:------------|
| `pipenv install` | Installs from a `Pipfile`. If there's no Pipfile, creates one and generates the basic skeleton |
| `pipenv install <package>` | Installs a package. Rather than using raw `pip`, `pipenv` will be used. This will install the package into the virtualenv, and will add it to the `Pipfile`. |
| `pipenv install <package> --dev` | Installs a dev package |
| `pipenv lock` | Regenerates `Pipenv.lock` file |
| `pipenv install --ignore-pipenv` | This will create and environment and install packages listed in `Pipfile.lock` ignoring `Pipfile` file. This is useful, for examplel, to make deployments in production |
| `pipenv uninstall` | Removes the packages pedified in the `Pipfile` |

## Working with venvs

| Commands         | Description | 
|:-----------------|:------------|
| `pipenv install` | Creates a new venv and installs all packages within `Pipfile`. If there's no Pipfile / venv, it will generate one. |
| `pipenv --venv` | Locate current venv |
| `pipenv --rm` | Deletes current venv |


##  Interactive Commands

| Commands         | Description | 
|:-----------------|:------------|
| `pipenv shell` | Creates a shell within the virtualenv |
| `pipenv run <command>` | Runs a command within the virtualenv |

## Working with `requirements.txt` files

| Commands         | Description | 
|:-----------------|:------------|
| `pipenv install -r <requirements_file_path>` | Installs requirements from a requirements file |
| `pipenv lock -r` | Generates a requirements file from a pipfile | 

## Other useful commands

| Commands         | Description | 
|:-----------------|:------------|
| `pipenv check` | Perform PEP syntax checks and security and version checks |
| `pipenv graph` | Shows installed packages and dependencies among them |
