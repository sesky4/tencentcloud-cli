**Example 1: Querying purge history**



Input: 

```
tccli ecdn DescribePurgeTasks --cli-unfold-argument  \
    --PurgeType ur \
    --TaskId 1234567
```

Output: 
```
{
    "Response": {
        "RequestId": "4d5a83f8-a61f-445b-8036-5636be640bef",
        "PushLogs": [
            {
                "TaskId": "153303185323131331",
                "Url": "http://www.test.com/",
                "Status": "Done",
                "PurgeType": "url",
                "FlushType": "flush",
                "CreateTime": "2018-07-30 18:10:53"
            }
        ],
        "TotalCnt": 20
    }
}
```
