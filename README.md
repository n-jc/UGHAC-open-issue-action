# Open Issue Action

[![GitHub Super-Linter](https://github.com/n-jc/UGHAC-open-issue-action/actions/workflows/linter.yml/badge.svg)](https://github.com/super-linter/super-linter)
![CI](https://github.com/n-jc/UGHAC-open-issue-action/actions/workflows/ci.yml/badge.svg)

This action opens a new issue on GitHub with a title, body and a list of
assignees.

## Inputs

### `token`

**Required** A GitHub token with issues:write scope.

### `title`

**Required** The title of the issue

### `body`

The body of the issue.

### `assignees`

A list of GitHub usernames to assign to the issue.

## Outputs

### `issue`

The created issue object as a json string.

## Example usage

```yaml
uses: n-jc/UGHAC-open-issue-action@v1
  id: issue
  with:
    token: ${{ secrets.GITHUB_TOKEN }}
    title: Test Issue
    body: Test issue body
    assignees: |
      n-jc
```
