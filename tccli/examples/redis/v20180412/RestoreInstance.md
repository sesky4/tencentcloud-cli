**Example 1: Restoring a Redis Instance**



Input: 

```
tccli redis RestoreInstance --cli-unfold-argument  \
    --InstanceId crs-5a4py64p \
    --Password mypassword \
    --BackupId 678362566696298532848117
```

Output: 
```
{
    "Response": {
        "TaskId": "6954227",
        "RequestId": "4daddc97-0005-45d8-b5b8-38514ec1e97c"
    }
}
```
