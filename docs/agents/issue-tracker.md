# Issue tracker: GitHub

Issues and specs for this repo live as GitHub Issues. Use the `gh` CLI for all operations.

Repository: `diepvicuong/my-portfolio`

## Conventions

- Create an issue with `gh issue create`.
- Read an issue with `gh issue view <number> --json number,title,body,labels,comments`.
- List issues with `gh issue list` and the appropriate state or label filters.
- Comment with `gh issue comment <number> --body "..."`.
- Apply or remove labels with `gh issue edit <number> --add-label` or `--remove-label`.
- Close an issue with `gh issue close <number> --comment "..."`.

## Pull requests as a request surface

PRs as a request surface: no.

## Wayfinding operations

The Wayfinder map is a single GitHub issue labelled `wayfinder:map`; its decision tickets are child issues labelled `wayfinder:research`, `wayfinder:prototype`, `wayfinder:grilling`, or `wayfinder:task`.

- Create a map with `gh issue create --label wayfinder:map`.
- Link child issues as sub-issues of the map when supported; otherwise put the parent reference in the child body.
- Use GitHub native issue dependencies for blocking relationships where available.
- Claim a ticket by assigning it before doing work.
- Resolve a ticket by posting the answer as a comment, closing the issue, and appending a context pointer to the map's `Decisions so far` section.

## When a skill says “publish to the issue tracker”

Create a GitHub issue.
