**Example 1: 查询固件升级任务状态分布**



Input: 

```
tccli iotcloud DescribeFirmwareTaskDistribution --cli-unfold-argument  \
    --ProductId O4CCMMZE3A \
    --TaskId 112 \
    --FirmwareVersion 1.0
```

Output: 
```
{
    "Response": {
        "StatusInfos": [
            {
                "Total": 1,
                "Status": 0
            },
            {
                "Status": 5,
                "Total": 1
            },
            {
                "Total": 1,
                "Status": 6
            }
        ],
        "RequestId": "25a4a01b-8146-4388-90f9-2d8ca18bbb1f"
    }
}
```

