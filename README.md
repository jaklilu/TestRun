# Cancel Azure Subscription helpers

These scripts create a policy exemption, grant Owner, cancel a subscription, and verify the result.

## Required environment variables

Both scripts fail with a clear error if any of these are unset.

| Variable | PowerShell | Python |
| --- | --- | --- |
| `AZURE_SUBSCRIPTION_ID` | `$env:AZURE_SUBSCRIPTION_ID` | `os.environ` |
| `AZURE_USER_OBJECT_ID` | `$env:AZURE_USER_OBJECT_ID` | `os.environ` |
| `AZURE_MANAGEMENT_GROUP_ID` | `$env:AZURE_MANAGEMENT_GROUP_ID` | `os.environ` |

`AZURE_MANAGEMENT_GROUP_ID` is the management group segment used in the policy assignment resource path (`/providers/Microsoft.Management/managementGroups/<id>/...`).

Example:

```bash
export AZURE_SUBSCRIPTION_ID="<your-subscription-id>"
export AZURE_USER_OBJECT_ID="<your-user-object-id>"
export AZURE_MANAGEMENT_GROUP_ID="<your-management-group-id>"
```

PowerShell:

```powershell
$env:AZURE_SUBSCRIPTION_ID = "<your-subscription-id>"
$env:AZURE_USER_OBJECT_ID = "<your-user-object-id>"
$env:AZURE_MANAGEMENT_GROUP_ID = "<your-management-group-id>"
```
