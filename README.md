# Cancel Azure Subscription helpers

These scripts create a policy exemption, grant Owner, cancel a subscription, and verify the result.

## Required environment variable

Set **`AZURE_SUBSCRIPTION_ID`** to the Azure subscription to operate on. Both scripts fail with a clear error if it is unset.

PowerShell (`00-CreateExemption&CancelSub.ps1`) reads `$env:AZURE_SUBSCRIPTION_ID`.

Python (`Cancel-Azure-Subscription-Python/CreateExemption&CancelSub v1.py`) reads `os.environ["AZURE_SUBSCRIPTION_ID"]` (via `os.environ.get`).

Example:

```bash
export AZURE_SUBSCRIPTION_ID="<your-subscription-id>"
```

PowerShell:

```powershell
$env:AZURE_SUBSCRIPTION_ID = "<your-subscription-id>"
```
