github-workflow
===============

## Branching Model

There are two types of branching models. Which to use depends on the purpose of the repo.

### General Repos

If the repo is for general purposes, is a module or a pod, then it should follow the standard default of using `master` as the main branch. And changes should be committed on branches off of master, and then merged back in through pull requests.

### Production Repos

All repos that will deploy to production servers or be released as binaries should use the default branch of `develop`. Pull requests should be branches off of `develop`.

Branch | Explenation
--- | ---
develop | master development branch
qa | testing branch
staging | final pass of tests before production
production | production ready

If a hotfix is needed, you can open a PR directly into that branch. Once merged, the changes should then be merged back down to `develop`.
For example, if you hotfixed `staging`, once the changes are in `staging` then `staging` should be merged into `qa`, and then `qa` should be merged into `develop`.

## PR Branches

All development branches, regardless of repo type, should be prefixed with one of the following

Branch | Explenation
--- | ---
feature/ | feature / story
fix/ | bug fix
misc/ | anything that doesn't fit the above

## Labels

Label | Explenation
--- | ---
☆ EPIC | this feature is very big, has multiple smaller issues
♨︎ TBD | this feature is yet to be finalized
♺ WIP | somebody is shipping this
❝what if…❞ | the common question to ask when you have an idea
reaped | this issues has been closed due to being stale
P0 | critical, drop everything and fix it
P1 | servere bug, or high priority feature
P2 | general bug, or a general feature request
P3 | lowest priority, for bugs or features
bug | github default label - should be assigned to all bugs
duplicate | github default label - use when duplicate issues are closed
enhancement | github default label - use for features
help wanted | github default label - use when wanting help or feedback
invalid  | github default label - use if an issue is not accurate, before closing
question | github default label - use when asking a question
wontfix | github default label - use if closing an issue or pr when not resolving
