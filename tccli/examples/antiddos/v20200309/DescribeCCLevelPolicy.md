**Example 1: 获取CC分级策略**



Input: 

```
tccli antiddos DescribeCCLevelPolicy --cli-unfold-argument  \
    --InstanceId bgpip-0000011x \
    --Ip 1.3.2.5 \
    --Domain 1.sca.com \
    --Protocol HTTP
```

Output: 
```
{
    "Response": {
        "RequestId": "5063ab0a-a8a7-41e8-ace2-263b2c1c8794",
        "Level": "loose"
    }
}
```

