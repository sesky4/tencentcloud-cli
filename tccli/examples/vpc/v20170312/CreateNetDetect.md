**Example 1: Creating a network detection instance**



Input: 

```
tccli vpc CreateNetDetect --cli-unfold-argument  \
    --Version 2017-03-12 \
    --VpcId vpc-12345678 \
    --SubnetId subnet-12345678 \
    --NetDetectName test \
    --DetectDestinationIp 10.0.0.2 10.0.0.3 \
    --NextHopType NORMAL_CVM \
    --NextHopDestination 10.0.0.4
```

Output: 
```
{
    "Response": {
        "NetDetect": {
            "VpcId": "vpc-12345678",
            "VpcName": "vpc-test",
            "SubnetId": "subnet-12345678",
            "SubnetName": "subnet-test",
            "NetDetectId": "netd-12345678",
            "NetDetectName": "test",
            "DetectDestinationIp": [
                "10.0.0.2",
                "10.0.0.3"
            ],
            "DetectSourceIp": [
                "10.0.0.5",
                "10.0.0.6"
            ],
            "NextHopType": "NORMAL_CVM",
            "NextHopDestination": "10.0.0.4",
            "NextHopName": "",
            "NetDetectDescription": "",
            "CreateTime": "0000-00-00 00:00:00"
        },
        "RequestId": "6aa316a4-07d2-4355-b87d-40b7f22972b0"
    }
}
```
