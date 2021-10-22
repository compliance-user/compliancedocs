# Compliance Controls Repository Workflow

Branches
---
    dev
    ---
    int
    ---
    qa
    ---
    sandbox
    ---
    prod

Request POST or PUT
---
<h6>Tenant ID is created through corestack UI, the ID alone will be sent to github to trigger the pipeline</h6>

# Code snippet

```python
from github import Github

def execute_compliance(token, branch_ref):
    try:
        g = Github(login_or_token=token)
        repo = g.get_repo('Corestacklabs/Controls')
        contents = repo.get_contents("tenant_list.json", ref=branch_ref)
        return repo, contents
    except Exception as e:
        LOG.error(e.message)
```