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
