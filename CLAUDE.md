# git_push

This repository exists to hold the daily commit streak log. There is no
application code here.

## Daily commit routine

A scheduled task appends the current date to `daily-commit-log.md` and pushes.

Two things are required for that commit to register on the GitHub contribution
graph for `rraj005`. Both have been gotten wrong before:

1. **Author identity.** The container's default git identity is
   `Claude <noreply@anthropic.com>`, which is not associated with the
   `rraj005` account, so commits authored with it never appear on the graph.
   Set the identity before committing:

   ```
   git config user.name "Raunit Raj"
   git config user.email "211502195+rraj005@users.noreply.github.com"
   ```

   The `users.noreply.github.com` address is tied to the account and keeps the
   personal email out of public history.

2. **Branch.** GitHub only counts commits on the default branch, or on a branch
   with an open pull request. The repository owner has authorized pushing these
   daily commits **directly to `main`**; no pull request is needed for them.
   This authorization covers the daily streak commit in this repository only.
