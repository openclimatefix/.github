# .github

Various Community and Code Health Files.

## Issue and PR Templates

Found in `.github/ISSUE_TEMPLATE` and `./PULL_REQUEST_TEMPLATE.md` respectively. These files are used across the organisation as [issue templates](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests).

## Organisation Profile README

Can be found in `.profile/README.md` and is rendered by GitHub on the [OCF organisation page](https://github.com/openclimatefix/).

## Reusable Workflows

To reduce duplication, we offer a set of reusable workflows that are used across most of our repositories. The following workflows can be found in `.github/workflows/`:

- `python-lint`: Runs `isort`, `flake8`, `black` and `pydocstyle`
- **COMING SOON** `python-test`: Runs `pytest` and `pydoctest`
- **COMING SOON** `release`: Runs a release script

You can use these workflows in any other workflow using the syntax `{owner}/{repo}/{path}/{filename}@{ref}`. For example:

```yaml
name: Lint Python
on: [push]
jobs:
  call-run-python-linters:
    uses: openclimatefix/.github/.github/workflows/python-lint.yml@main
```

You can [learn more about reusable workflows in the GitHub docs](https://docs.github.com/en/actions/learn-github-actions/reusing-workflows).
