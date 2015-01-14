github-workflow
===============

## Branching Model

All development repos should use the default branch of `develop`. Pull requests should be branches off of `develop`.

```
- `develop`     // master development branch
- `qa`          // testing branch
- `staging`     // final pass of tests before production
- `production`
```

If a hotfix is needed, you can open a PR directly into that branch. Once merged, the changes should then be merged back down to `develop`.
For example, if you hotfixed `staging`, once the changes are in `staging` then `staging` should be merged into `qa`, and then `qa` should be merged into `develop`.

## PR Branches

All development branches should be prefixed with one of the following

```
- feature/      // feature / story
- fix/          // bug fix
- misc/         // anything that doesn't fit the above
```

## Labels

```
- ☆ EPIC        // this feature is very big, has multiple smaller issues
- ♨︎ TBD         // this feature is yet to be finalized
- ♺ WIP         // somebody is shipping this
- ❝what if…❞    // the common question to ask when you have an idea
- reaped        // this issues is reaped before

// github default's 
- `bug`
- `duplicate`
- `enhancement`
- `help wanted`
- `invalid`
- `question`
- `wontfix`
```

### Milestones
Used for major release milestone
