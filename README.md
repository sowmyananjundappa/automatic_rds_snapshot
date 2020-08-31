#rbs-snaps-copy-to-logs

## What's this for ?

Code from this module create a Lambda function with cross-account IAM roles which does the following, in order:
- retrieves the latest available RDS snapshot of a given server,
- copies the newly created destination RDS snapshot (different region) within account.
- shares the afore mentioned source RDS snapshot into different account.
- tags the newly created destination RDS snapshot with timestamps of its original creation (current account) and share (into different account).

In addition, the Lambda function has a capability of cleaning up snapshots older than a defined retention period (like 90 days), which works by setting the environment variable ACTION = "CLEANUP".

## Anything else ?

//TODO: encryption ?
