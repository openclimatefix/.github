# Python Coding Style

## Package management
We use [uv](https://astral.sh/uv/) to handle creation of reproducible environments and packaging of code. All projects should use a source-layout: either use the ocf-template repository as a base or run `uv init --package your-new-package-name` to start a new repository with the correct project structure.

## Code formatting
We use [Ruff](https://astral.sh/ruff/) for formatting and code linting, such as docstrings, import sorting, and flake8. The `.pyproject.toml` in our repository template has the configuration that we use across all our repositories. This also allows easy local usage, as the only command that needs to run is `ruff check --fix` or `ruff format` for code to be formated, linted, and some of the issues auto-fixed. 

### Docstrings
We use [Google-style docstrings](https://google.github.io/styleguide/pyguide.html#s3.8-comments-and-docstrings).

## Unittesting
In terms of requirements around unittesting etc, please see [our Pull Request template](https://github.com/openclimatefix/.github/blob/master/PULL_REQUEST_TEMPLATE.md) (which lists all the criteria we hope each pull request satisfies).

## Jupyter Notebooks
For now, we maintain the `.py` files, and try to ensure they're all internally consistent, but we don't promise to maintain all our notebooks!  (That might change if our code starts being used by lots of people!)

## Spelling
We use American English in our code (for example, so we use 'center' rather than 'centre').  This is true for variable namings and docstrings.

## Repository Template
If making a new OCF Repository, please try using our [template here](https://github.com/openclimatefix/ocf_template) which should help with boilerplate linting and setup. 
