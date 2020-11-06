**Example 1: Querying the information of supported customer gateway vendors**



Input: 

```
tccli vpc DescribeCustomerGatewayVendors --cli-unfold-argument  \
    --Version 2017-03-12
```

Output: 
```
{
    "Response": {
        "CustomerGatewayVendorSet": [
            {
                "Platform": "ios",
                "SoftwareVersion": "V15.4",
                "VendorName": "cisco"
            },
            {
                "Platform": "comware",
                "SoftwareVersion": "V1.0",
                "VendorName": "h3c"
            }
        ],
        "RequestId": "ccda8bff-d7aa-4a16-8a72-13e72a116205"
    }
}
```
