# pip-template

A template repository for creating a pip installable Python package.

Create a new conda environment with

```
conda create -n "your_package" python=3.10 pip
```

Activate it

```
conda activate your_package
```

Install your package in editable mode

```
pip install -r requirements.txt
```

## Add pre-commit hooks

Install pre-commit

```
pip install pre-commit
```

Adjust the `.pre-commit-config.yaml` file.
If you want to use pylint and/or black, install them with

```
pip install pylint
```

and

```
pip install black
```

Adjust the `.pylintrc` file with rules that you want to exclude.

Now install the git hooks with

```
pre-commit install
```

Try running pre-commit against all files

```
pre-commit run --all-files
```

## Documentation with Sphinx

Install spinx
```
pip install sphinx
```

Install readthedocs theme
```
pip install sphinx-rtd-theme
```

### Update default files

Navigate to `docs` and run
```
sphinx-quickstart
```

## Build docs

```
sphinx-build -b html docs/source docs/build
```
