**Example 1: 新增单个镜像仓库详细信息**

新增单个镜像仓库详细信息

Input: 

```
tccli tcss AddAssetImageRegistryRegistryDetail --cli-unfold-argument  \
    --Username usename \
    --Name admin \
    --Url http://127.0.0.1:8080 \
    --RegistryVersion V2 \
    --RegistryRegion default \
    --NetType public \
    --Password password \
    --RegistryType harbor
```

Output: 
```
{
    "Response": {
        "HealthCheckErr": "connect closed",
        "NameRepeatErr": "name repeat err",
        "RegistryId": 1002,
        "RequestId": "f8d97649-ca1b-4f94-8ed4-40052a40d426"
    }
}
```

