# Python Script
Example for a python project repository

Here is the general structure of this setup. Below are quick instructions of things to change for your new repository:
```
template_python_library/                      
    template_python_library/ 
        __init__.py
        files.py
        modules/
            __init__.py
            more_files.py
    
    .github/
        ISSUE_TEMPLATE/
            bug_report.md # template for filing bugs
            feature_request.md # template for feature requests
        workflows/
            build-test.yml 
                # github actions workflow to:
                #   - test linting/formating
                #   - build & test the package
                # To work, this requires a number of the Make commands to 
                # be setup, including: dev, requirements, lint, test
    
    docs/
        # folder where the docs will be built
    
    examples/ 
        # folder where example scripts should be placed. 
        # e.g., https://github.com/gattia/cycpd/tree/main/examples
    
    .gitignore
        # pre-filled gitignore file for common python packages & specific to this repo. 
    
    Makefile
        # makefile with convenienience commands designed to make 
        # developing/installing easier. 
    
    pyproject.toml
        # file to specify metadata of the project, requirements, etc. 
        # this replaces `setup(...)` in a normal `setup.py` file. 
        # also includes description of configurations for other build tools
        # such as linting, (isort, black). 
        # information for setting up `pyproject.toml`: https://peps.python.org/pep-0621/
        # other helpful resources: 
        #    https://setuptools.pypa.io/en/latest/userguide/pyproject_config.html
        #    https://scikit-hep.org/developer/pep621


    README.md 
        # current background info, install info, and how to contribute

    setup.py 
        # file to call to build library `python setup.py install`
        # setup.py is no longer encouraged. We provide the most basic one here
        # because it is still needed to install in editable mode.This is only 
        # needed for editable mode because `pyproject.toml` does not fully support 
        # editable mode, yet:
        #   https://setuptools.pypa.io/en/latest/userguide/quickstart.html#development-mode
        #
        # also, the setup.py might be needed for installing cython dependencies
        # Example here: https://github.com/gattia/cycpd/blob/e235da5276652eea12875aef3c8280a9b673122e/setup.py#L12-L20
        # and here: https://github.com/gattia/cycpd/blob/e235da5276652eea12875aef3c8280a9b673122e/setup.py#L48
    
    requirements.txt
        # packages that this repository requires/ that should be installed first 
        # this is necessary to let conda install dependencies (as well as pip). 
        # These requirements could be placed inside of the pyproject.toml
        #     - But can conda read the pyproject.toml?

    CONTRIBUTING.md 
        # information about how to contribte to the library
        # this format overall was bored from DOSMA
    
    LICENSE
        # Package license / license type. 
```
