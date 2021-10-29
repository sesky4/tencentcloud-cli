**Example 1: 调用成功示例**



Input: 

```
tccli tiia SearchImage --cli-unfold-argument  \
    --ImageUrl http://crawl.ws.126.net/img/999674ed516ef903e486cd2ff83e1d2f.jpg \
    --Filter value > 10 \
    --MatchThreshold 1 \
    --Limit 30 \
    --Offset 0 \
    --GroupId work
```

Output: 
```
{
    "Response": {
        "Count": 2,
        "ImageInfos": [
            {
                "CustomContent": "",
                "EntityId": "test2",
                "PicName": "3001",
                "Score": 0,
                "Tags": "{\"value\": 15}"
            },
            {
                "CustomContent": "",
                "EntityId": "test2",
                "PicName": "3002",
                "Score": 0,
                "Tags": "{\"value\": 20}"
            }
        ],
        "RequestId": "2d658a05-62d5-4f82-913c-50832146f6f3"
    }
}
```
