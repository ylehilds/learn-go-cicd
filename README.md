![<alt-text-here>](https://github.com/<OWNER>/<REPOSITORY>/actions/workflows/<WORKFLOW_FILE>/badge.svg)
# Deployment Pipeline flow
```mermaid
graph TD;
Write code-->Commit
Commit-->Push
Push-->"Pull Request"
"Pull Request"-->Review
Review-->Approve
Approve-->Merge
Merge-->GHA
GHA-->(CI Steps)
(CI Steps)-->(CD Build)
(CD Build)-->Push Image
Push Image-->
```
