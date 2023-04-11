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
*note: onboardingBranch & baseBranch has been modified & now there is a conflict
```log
// since baseBranch cache is invalid for isOnboarded()
DEBUG: isOnboarded() (repository=RahulGautamSingh-testing/onboarding-2)
DEBUG: Checking cached config file name (repository=RahulGautamSingh-testing/onboarding-2)
...
// fall back to git & extract cache removed
DEBUG: Onboarding PR already exists (repository=RahulGautamSingh-testing/onboarding-2)
DEBUG: Onboarding branch modified. Removing outdated extract cache for branch=main (repository=RahulGautamSingh-testing/onboarding-2)
DEBUG: isBranchConflicted(main, renovate/configure) (repository=RahulGautamSingh-testing/onboarding-2)
DEBUG: branch.isConflicted(): using git to calculate (repository=RahulGautamSingh-testing/onboarding-2)
DEBUG: Setting git author name: Renovate Bot (repository=RahulGautamSingh-testing/onboarding-2)
DEBUG: Setting git author email: renovate@whitesourcesoftware.com (repository=RahulGautamSingh-testing/onboarding-2)
DEBUG: setCachedConflictResult(): Branch cache not present (repository=RahulGautamSingh-testing/onboarding-2)
DEBUG: branch.isConflicted(): true (repository=RahulGautamSingh-testing/onboarding-2)
DEBUG: Update Onboarding Cache (repository=RahulGautamSingh-testing/onboarding-2)
       "onboardingCache": {
         "defaultBranchSha": "03556a031fd020ec72ed3047ef2cc31a4af7f7fc",
         "onboardingBranchSha": "ca66228ac1f42b07de209d06b5c9adf9faa1268b",
         "isConflicted": true
       }
...
DEBUG: Update Onboarding Cache (repository=RahulGautamSingh-testing/onboarding-2)
       "onboardingCache": {
         "defaultBranchSha": "03556a031fd020ec72ed3047ef2cc31a4af7f7fc",
         "onboardingBranchSha": "ca66228ac1f42b07de209d06b5c9adf9faa1268b",
         "isConflicted": true // updated 
       }
...
// FAULT DETECTED...WIP
```
