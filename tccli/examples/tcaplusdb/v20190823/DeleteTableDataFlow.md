**Example 1: 删除表格的数据订阅**

删除表格的数据订阅

Input: 

```
tccli tcaplusdb DeleteTableDataFlow --cli-unfold-argument  \
    --ClusterId 5674209986 \
    --SelectedTables.0.TableInstanceId tcaplus-1f224454 \
    --SelectedTables.0.TableGroupId 101 \
    --SelectedTables.0.TableName tb_example
```

Output: 
```
{
    "Response": {
        "RequestId": "122bb375-7464-4536-a3c5-8ddbdd6f4ce4",
        "TableResults": [
            {
                "Error": null,
                "TableGroupId": "101",
                "TableIdlType": null,
                "TableInstanceId": "tcaplus-1f224454",
                "TableName": "tb_example",
                "TableType": null,
                "ApplicationId": "null",
                "TaskId": "5674209986-1199",
                "TaskIds": null
            }
        ],
        "TotalCount": 1
    }
}
```

