github-workflow
===============

## Branching Model

There are two types of branching models. Which to use depends on the purpose of the repo.

### General Repos

If the repo is for general purposes, is a module or a pod, then it should follow the standard default of using `master` as the main branch. And changes should be committed on branches off of master, and then merged back in through pull requests.

### Production Repos

All repos that will deploy to production servers or be released as binaries should use the default branch of `develop`. Pull requests should be branches off of `develop`.

```
- `develop`     // master development branch
- `qa`          // testing branch
- `staging`     // final pass of tests before production
- `production`
```

If a hotfix is needed, you can open a PR directly into that branch. Once merged, the changes should then be merged back down to `develop`.
For example, if you hotfixed `staging`, once the changes are in `staging` then `staging` should be merged into `qa`, and then `qa` should be merged into `develop`.

## PR Branches

All development branches, regardless of repo type, should be prefixed with one of the following

```
- feature/      // feature / story
- fix/          // bug fix
- misc/         // anything that doesn't fit the above
```

## Labels

```
- `☆ EPIC`      // this feature is very big, has multiple smaller issues
- `♨︎ TBD`       // this feature is yet to be finalized
- `♺ WIP`       // somebody is shipping this
- `❝what if…❞`  // the common question to ask when you have an idea
- `reaped`      // this issues has been closed due to being stale

// bug priorities
- `P0`          // critical bug, drop everything and fix it
- `P1`          // severe bug, must be fixed
- `P2`          // general bug, should be fixed, prioritize accordingly

// github default's 
- `bug`
- `duplicate`
- `enhancement`
- `help wanted`
- `invalid`
- `question`
- `wontfix`
```
