**Example 1: 无**



Input: 

```
tccli dcdb CreateHourDCDBInstance --cli-unfold-argument  \
    --ShardMemory 2 \
    --ShardStorage 10 \
    --ShardNodeCount 2 \
    --ShardCount 2
```

Output: 
```
{
    "Response": {
        "RequestId": "14f6980a-7fe1-11ea-b896-525400542aa6",
        "InstanceIds": [
            "tdsql-xxxxxx"
        ],
        "FlowId": 1122
    }
}
```
