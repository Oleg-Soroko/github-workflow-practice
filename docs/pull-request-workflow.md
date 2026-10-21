# Practice the pull request workflow

A pull request proposes a branch for merging and keeps the explanation, changes, and discussion together. Practice with a useful documentation update, such as clarifying a confusing step or correcting a broken link.

## Prepare a focused change

1. Start a new branch from the current `main` branch. In GitHub's file editor, select the option to create a new branch when committing your edit.
2. Make one coherent change and give the commit a descriptive message.
3. If the change adds a feature, setup step, or control, update the README in the same branch.

## Open the pull request

1. Open **Pull requests → New pull request**.
2. Set the base branch to `main` and select your change branch as the comparison branch.
3. Explain the problem, what changed, and how you checked the result. The repository's PR template provides these fields automatically for future pull requests.
4. If the PR completes an issue, add `Closes #NUMBER` to the description.

## Check and merge

1. Open **Files changed** and confirm that every changed file belongs to the task.
2. Check Markdown links and read the instructions as a new reader would.
3. Resolve merge conflicts and any required checks. Request a review when the change needs another person's input.
4. Use **Merge pull request** when the change is ready.
5. Confirm that the PR says **Merged** and that the changes appear on `main`.

## Optional terminal workflow

With Git and GitHub CLI installed and authenticated, the following is the equivalent workflow. Choose a unique branch name for each task.

```powershell
git switch -c docs/clarify-setup
# Edit the relevant files, then stage those files explicitly.
git add README.md
git diff --cached --check
git commit -m "docs: clarify the setup instructions"
git push -u origin docs/clarify-setup
gh pr create --base main --fill
```

Inspect the PR on GitHub before merging. This guide intentionally leaves the merge as a deliberate UI step.

[Return to the README](../README.md)
