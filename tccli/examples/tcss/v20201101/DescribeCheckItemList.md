**Example 1: 查询所有检查项示例**



Input: 

```
tccli tcss DescribeCheckItemList --cli-unfold-argument  \
    --Offset 0 \
    --Limit 10
```

Output: 
```
{
    "Response": {
        "ClusterCheckItems": [
            {
                "AffectedType": "Workload",
                "AffectedVersion": "所有",
                "CVENumber": "CVE-2021-26691",
                "CVSS": "AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H",
                "CVSSScore": "9.8",
                "CheckItemId": 10280,
                "DiscoverTime": "2023-08-11 11:18:23",
                "IgnoredAssetNum": 0,
                "IsIgnored": false,
                "ItemDetail": "default ServiceAccount禁止授予写入/修改权限",
                "Name": "禁止授予ServiceAccount default写入/修改权限",
                "RelateLink": "https://",
                "RiskAssessment": "assess***",
                "RiskAttribute": "MaliciousTampering",
                "RiskLevel": "High",
                "RiskProperty": "instance-sfd***",
                "RiskTarget": "RBAC",
                "RiskType": "ConfigRisk",
                "Solution": "确保 default 名称的ServiceAccount禁止授予写入/修改权限"
            }
        ],
        "RequestId": "3d286d4b-8df0-4247-af69-02b510fac784",
        "TotalCount": 163
    }
}
```

