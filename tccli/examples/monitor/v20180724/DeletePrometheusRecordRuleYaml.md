**Example 1: 删除聚合规则**

删除聚合规则

Input: 

```
tccli monitor DeletePrometheusRecordRuleYaml --cli-unfold-argument  \
    --InstanceId prom-ejfdgh \
    --Names test-rule
```

Output: 
```
{
    "Response": {
        "RequestId": "eac6b301-a322-493a-8e36-83b295459397"
    }
}
```

