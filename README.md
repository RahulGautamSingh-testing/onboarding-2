# onboarding-2

Create onboarding PR. Update baseBranch with new deps. Modify `chartfile.yaml` to create conflict.

## Expectations:
  - Updates PR body to show new deps without rebasing 
  - Adds a comment to inform user about conflict

## Observations:
  - Updates PR body to show new deps without rebasing ✅
  - Adds a comment to inform user about conflict
  
## Relevant logs:

### Second Run
*note: this is the run after updating baseBranch ie. adding `package.json`

```log
DEBUG: extract() (repository=RahulGautamSingh-testing/onboarding-2)
DEBUG: Cached extract result cannot be used due to base branch SHA change (old=374e56, new=8a7c51) 
...
DEBUG: PR updated...prNo: 1 (repository=RahulGautamSingh-testing/onboarding-2)
 INFO: Onboarding PR updated (repository=RahulGautamSingh-testing/onboarding-2)
       "pr": 1
```

### Third run
*note: onboardingBranch has been modified & now there is a conflict
```log
DEBUG: branch.isModified(): using git to calculate (repository=RahulGautamSingh-testing/onboarding-2)
...
DEBUG: branch.isModified() = true (repository=RahulGautamSingh-testing/onboarding-2)
..
DEBUG: Onboarding branch modified. Removing outdated extract cache for branch=main (repository=RahulGautamSingh-testing/onboarding-2)
DEBUG: isBranchConflicted(main, renovate/configure) (repository=RahulGautamSingh-testing/onboarding-2)
DEBUG: branch.isConflicted(): using git to calculate (repository=RahulGautamSingh-testing/onboarding-2)
DEBUG: Setting git author name: Renovate Bot (repository=RahulGautamSingh-testing/onboarding-2)
DEBUG: Setting git author email: renovate@whitesourcesoftware.com (repository=RahulGautamSingh-testing/onboarding-2)
DEBUG: setCachedConflictResult(): Branch cache not present (repository=RahulGautamSingh-testing/onboarding-2)
DEBUG: branch.isConflicted(): true (repository=RahulGautamSingh-testing/onboarding-2)
DEBUG: Update Onboarding Cache (repository=RahulGautamSingh-testing/onboarding-2)
       "onboardingCache": {
         "defaultBranchSha": "2d6a72c976d2581a6e14fcb67f34454225986696",
         "onboardingBranchSha": "0360d7485a8778b26b935be19e629c9dcb3080ef",
         "isConflicted": true,
         "isModified": true
       }
```
