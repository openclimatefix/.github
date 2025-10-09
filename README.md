# .github

Configuration and documentation for the Open Climate Fix GitHub organisation.

## Issue and PR Templates

Found in `.github/ISSUE_TEMPLATE` and `./PULL_REQUEST_TEMPLATE.md` respectively. These files are used across the organisation as [issue templates](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests).

## Organisation Profile README

Can be found in `.profile/README.md` and is rendered by GitHub on the [OCF organisation page](https://github.com/openclimatefix/).

## Reusable Workflows

To reduce duplication, we offer a set of reusable workflows that are used across most of our repositories. The following workflows can be found in `.github/workflows/`:

- `branch_ci`: Lints, tests, and optionally containerizes python code (to be used on pushes to non-default branches).
- `bump_tag`: Creates a new semantically versioned tag (to be used on merges to the default branch).
- `tagged_ci`: Publishes containers and wheels (to be used on pushes to semantic tags)

You can use these workflows in any other workflow using the syntax `{owner}/{repo}/{path}/{filename}@{ref}`. For example:

```yaml
name: Branch CI
on:
  push:
    branches-ignore: ["main"]
jobs:
  run-ci:
    uses: openclimatefix/.github/.github/workflows/branch_ci@main
```

You can [learn more about reusable workflows in the GitHub docs](https://docs.github.com/en/actions/learn-github-actions/reusing-workflows).
