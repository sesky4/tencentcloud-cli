**Example 1: 查询web服务列表**

查询web服务列表

Input: 

```
tccli tcss DescribeAssetWebServiceList --cli-unfold-argument ```

Output: 
```
{
    "Response": {
        "List": [
            {
                "ServiceID": "abc",
                "HostID": "abc",
                "HostIP": "abc",
                "ContainerName": "abc",
                "Type": "abc",
                "Version": "abc",
                "RunAs": "abc",
                "Listen": [
                    "abc"
                ],
                "Config": "abc",
                "ProcessCnt": 1,
                "AccessLog": "abc",
                "ErrorLog": "abc",
                "DataPath": "abc",
                "WebRoot": "abc",
                "Pids": [
                    1
                ],
                "MainType": "abc",
                "Exe": "abc",
                "Parameter": "abc",
                "ContainerId": "abc",
                "HostName": "abc",
                "PublicIp": "abc",
                "NodeID": "abc",
                "PodIP": "abc",
                "PodName": "abc",
                "NodeType": "abc",
                "NodeUniqueID": "abc"
            }
        ],
        "TotalCount": 1,
        "RequestId": "abc"
    }
}
```

