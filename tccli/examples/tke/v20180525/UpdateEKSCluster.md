**Example 1: 修改弹性集群**

修改弹性集群

Input: 

```
tccli tke UpdateEKSCluster --cli-unfold-argument  \
    --ServiceSubnetId subnet-xxxx \
    --ClusterName test_cluster1 \
    --SubnetIds subnet-xxxx \
    --ClusterId cls-xxxxxx \
    --DnsServers.0.Domain exam.com \
    --DnsServers.0.DnsServers 10.2.2.88:53 \
    --ClusterDesc my_test_cluster888
```

Output: 
```
{
    "Response": {
        "RequestId": "eac6b301-a322-493a-8e36-83b295459397"
    }
}
```

