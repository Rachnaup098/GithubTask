# Git & GitHub Practice Log

## About This Portfolio

This repository documents my hands-on practice with Git and GitHub.

It includes commands, concepts, errors, solutions, and links to practical work.

## Repository Links

- Main Practice Portfolio: https://github.com/Rachnaup098/GithubTask
- Hello-World Practice Repository: https://github.com/Rachnaup098/Hello-World
- Pull Request Practice: https://github.com/Rachnaup098/Hello-World/pull/11600
- README Improvement Issue: https://github.com/Rachnaup098/GithubTask/issues/2

## Practice 1: Repository Status

**Task:** Check the current Git repository status.

**Commands used:**

```bash
git status
```

**Result:** The `main` branch was up to date with `origin/main`, and the working tree was clean.

**Repository:** GithubTask

## Practice 2: Fork and Pull Request

**Task:** Practice making a change in a fork and creating a Pull Request.

**Repository:** Hello-World

**Branch:** `my-first-change`

**Commit:** `f22ccda` - Update README for first pull request

**Proof:** https://github.com/Rachnaup098/Hello-World/pull/11600

## Practice 3: Merge Conflict

**Task:** Practice resolving a merge conflict.

**Repository:** Hello-World

**Branch:** `conflict-practice`

**Commit:** `3f27f48` - Resolve README merge conflict

**What I learned:** When two branches change the same part of a file, Git may require manual conflict resolution before the changes can be combined.

## Practice 4: Revert a Commit

**Task:** Practice undoing a commit with `git revert`.

**Repository:** Hello-World

**Original commit:** `3305c9d` - Add revert practice file

**Revert commit:** `d8b4fe5` - Revert "Add revert practice file"

**What I learned:** `git revert` creates a new commit that reverses an earlier commit.

## Practice 5: Recover a Deleted Branch

**Task:** Practice recovering a deleted branch using Git history.

**Repository:** Hello-World

**Commit to recover:** `53d0e56` - Add deleted branch practice file

**Method practiced:** Find the commit using the reflog, then recreate the branch from that commit.

**Note:** This was local practice. Remote publication must be verified separately.

## Practice 6: Reset and Commit Recovery

**Task:** Practice reset options and finding a commit that is no longer referenced by a branch.

**Repository:** Hello-World

**Commands practiced:**

```bash
git reset --soft HEAD~1
git reset --mixed HEAD
git reset --hard HEAD
git fsck --no-reflogs
```

**Recovered commit:** `444f620`

**Recovery branch:** `recovered-commit`

**What I learned:** Reset options affect the branch, staging area, and working files differently. Git recovery tools may help locate commits that are no longer referenced by a branch.

**Note:** These exercises were performed locally. They should not be described as remote changes unless verified.

## Practice 7: Rebase and Abort

**Task:** Practice handling a rebase conflict and safely aborting the rebase.

**Repository:** Hello-World

**Branches:** `rebase-practice` and `rebase-conflict-branch`

**Commands practiced:**

```bash
git rebase rebase-conflict-branch
git status
git rebase --abort
```

**What I learned:** If a rebase encounters conflicts, `git rebase --abort` can return the repository to its pre-rebase state.

## Practice 8: Git Fetch and Remotes

**Task:** Practice fetching updates from an upstream repository.

**Repository:** Hello-World

**Remotes:**
- `origin`: my fork
- `upstream`: the original repository

**Commands practiced:**

```bash
git remote -v
git fetch upstream
```

**What I learned:** `git fetch` downloads remote updates without automatically merging them into the current branch.

## Errors and Troubleshooting

### Error: `gitfetch: command not found`

**Cause:** The command was typed without a space.

**Correct command:**

```bash
git fetch upstream
```

### Error: `Could not resolve host`

**Cause:** Git could not resolve the remote hostname at that time. A network or remote URL issue needed checking.

**Troubleshooting commands:**

```bash
git remote -v
git fetch upstream
```

## Record-Keeping Policy

- Add verified commit IDs and links wherever available.
- Record local-only exercises honestly as local practice.
- Use actual dates from Git history or other reliable records; do not invent dates.
- Add new exercises to this file as practice continues.
