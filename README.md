![<alt-text-here>](https://github.com/<OWNER>/<REPOSITORY>/actions/workflows/<WORKFLOW_FILE>/badge.svg)
# Deployment Pipeline flow
```mermaid
---
config:
      theme: redux
---
graph TD;
Code([Write Code])-->Commit
Commit --> Push
Push --> PR["Pull Request"]
PR --> Review
Review --> Approve
Approve --> Merge
Merge --> GHA
GHA --> CI["CI Steps"]
CI --> CD["CD Build"]
CD --> Image["Push Image"]
Image-->Deploy
Deploy --> Operate
Operate --> Inform["Inform Requirements"]
Inform --> Code
```
