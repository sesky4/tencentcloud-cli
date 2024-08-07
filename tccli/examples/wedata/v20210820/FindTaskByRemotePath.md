**Example 1: 远端路径查找任务**

远端路径查找任务

Input: 

```
tccli wedata FindTaskByRemotePath --cli-unfold-argument  \
    --RemotePath /datastudio/project/1470547050521227264/peanut/test/1111.sh
```

Output: 
```
{
    "Response": {
        "RequestId": "111",
        "TaskDTOs": [
            {
                "TaskId": "20230516110202850",
                "VirtualTaskId": null,
                "VirtualFlag": false,
                "TaskName": "1111",
                "WorkflowId": "b5cc016e-e37c-11ed-8909-bc97e105ba60",
                "RealWorkflowId": null,
                "WorkflowName": "test",
                "FolderId": null,
                "FolderName": null,
                "CreateTime": "2023-05-16 11:02:02",
                "LastUpdate": "2023-05-16 11:02:06",
                "Status": "NS",
                "InCharge": "100028578753",
                "InChargeId": "100028578753",
                "StartTime": "2023-05-16 11:02:02",
                "EndTime": "2099-12-31 23:59:59",
                "ExecutionStartTime": "00:00",
                "ExecutionEndTime": "23:59",
                "ProjectId": "1470547050521227264",
                "ProjectIdent": null,
                "ProjectName": null,
                "CycleType": "DAY_CYCLE",
                "CycleStep": 1,
                "CrontabExpression": null,
                "DelayTime": 0,
                "StartupTime": 0,
                "RetryWait": 5,
                "Retriable": 1,
                "TaskAction": "",
                "TryLimit": 5,
                "RunPriority": 6,
                "TaskType": {
                    "TypeId": 35,
                    "TypeDesc": "Shell",
                    "CreateTime": "2022-02-12 11:13:41",
                    "SourceServerType": null,
                    "TargetServerType": null,
                    "RunJarName": "IdexShell.jar",
                    "TypeSort": "数据计算",
                    "InCharge": "admin",
                    "BrokerParallelism": 10,
                    "TaskParallelism": 10,
                    "DoRedoParallelism": 10000,
                    "DowngradePriorityTries": 2,
                    "RetryWait": 5,
                    "RetryLimit": 5,
                    "DefaultAliveWait": 720,
                    "PollingSeconds": 5,
                    "ParamList": "<parameters><parameter><name>hdpClient</name><value>/usr/hdp/current/hadoop-client</value></parameter><parameter><name>hiveClient</name><value>/usr/hdp/current/hive-client</value></parameter></parameters>",
                    "FileType": null,
                    "SelectFilePath": null,
                    "ExcludeCommonLib": false,
                    "PostHooks": null,
                    "KillAble": 0
                },
                "BrokerIp": "any",
                "ClusterId": null,
                "MinDateTime": null,
                "MaxDateTime": null,
                "ExecutionTTL": -1,
                "SelfDepend": 2,
                "LeftCoordinate": 352.0,
                "TopCoordinate": 221.0,
                "TaskExt": null,
                "Properties": null,
                "Notes": null,
                "InstanceInitStrategy": "T_PLUS_0",
                "YarnQueue": null,
                "Alarm": null,
                "ScriptChange": false,
                "Submit": false,
                "LastSchedulerCommitTime": null,
                "NormalizedJobStartTime": null,
                "RecoverFreezeStartTime": null,
                "SourceServer": null,
                "TargetServer": null,
                "Tasks": null,
                "Creater": "peanutzhu",
                "DependencyRel": "and",
                "DependencyWorkflow": "no",
                "EventListenerConfig": null,
                "EventPublisherConfig": null,
                "VirtualTaskStatus": null,
                "RecycleTips": null,
                "RecycleUser": null,
                "NewOrUpdate": null,
                "Params": null,
                "TaskLinkInfo": null,
                "ImportResult": null,
                "ContentType": null,
                "TaskAutoSubmit": null,
                "ProductName": "DATA_DEV",
                "OwnId": "100028448903",
                "UserId": "100028578753",
                "TenantId": "1315051789",
                "UpdateUser": "peanutzhu",
                "UpdateTime": "2023-05-16 11:02:06",
                "UpdateUserId": "100028578753",
                "SchedulerDesc": null,
                "ResourceGroup": "default",
                "VersionDesc": null,
                "LinkId": null,
                "UserFileId": "3a693d01-6109-4e79-a239-2d65d37e57e9",
                "Alarms": null,
                "DependencyConfigList": null,
                "ImportErrMsg": null
            },
            {
                "TaskId": "20230516110303168",
                "VirtualTaskId": null,
                "VirtualFlag": false,
                "TaskName": "1111_20230516110303147",
                "WorkflowId": "b5cc016e-e37c-11ed-8909-bc97e105ba60",
                "RealWorkflowId": null,
                "WorkflowName": "test",
                "FolderId": null,
                "FolderName": null,
                "CreateTime": "2023-05-16 11:03:03",
                "LastUpdate": "2023-05-16 11:03:03",
                "Status": "N",
                "InCharge": "peanutzhu",
                "InChargeId": null,
                "StartTime": "2023-05-16 11:03:03",
                "EndTime": "2025-05-16 11:03:03",
                "ExecutionStartTime": null,
                "ExecutionEndTime": null,
                "ProjectId": "1470547050521227264",
                "ProjectIdent": null,
                "ProjectName": null,
                "CycleType": "DAY_CYCLE",
                "CycleStep": 1,
                "CrontabExpression": null,
                "DelayTime": 0,
                "StartupTime": 0,
                "RetryWait": 5,
                "Retriable": 1,
                "TaskAction": "",
                "TryLimit": 5,
                "RunPriority": 6,
                "TaskType": {
                    "TypeId": 35,
                    "TypeDesc": "Shell",
                    "CreateTime": "2022-02-12 11:13:41",
                    "SourceServerType": null,
                    "TargetServerType": null,
                    "RunJarName": "IdexShell.jar",
                    "TypeSort": "数据计算",
                    "InCharge": "admin",
                    "BrokerParallelism": 10,
                    "TaskParallelism": 10,
                    "DoRedoParallelism": 10000,
                    "DowngradePriorityTries": 2,
                    "RetryWait": 5,
                    "RetryLimit": 5,
                    "DefaultAliveWait": 720,
                    "PollingSeconds": 5,
                    "ParamList": "<parameters><parameter><name>hdpClient</name><value>/usr/hdp/current/hadoop-client</value></parameter><parameter><name>hiveClient</name><value>/usr/hdp/current/hive-client</value></parameter></parameters>",
                    "FileType": null,
                    "SelectFilePath": null,
                    "ExcludeCommonLib": false,
                    "PostHooks": null,
                    "KillAble": 0
                },
                "BrokerIp": "any",
                "ClusterId": null,
                "MinDateTime": null,
                "MaxDateTime": null,
                "ExecutionTTL": -1,
                "SelfDepend": 1,
                "LeftCoordinate": 100.0,
                "TopCoordinate": 100.0,
                "TaskExt": null,
                "Properties": null,
                "Notes": null,
                "InstanceInitStrategy": "T_PLUS_0",
                "YarnQueue": null,
                "Alarm": null,
                "ScriptChange": false,
                "Submit": false,
                "LastSchedulerCommitTime": null,
                "NormalizedJobStartTime": null,
                "RecoverFreezeStartTime": null,
                "SourceServer": null,
                "TargetServer": null,
                "Tasks": null,
                "Creater": "peanutzhu",
                "DependencyRel": "and",
                "DependencyWorkflow": "no",
                "EventListenerConfig": null,
                "EventPublisherConfig": null,
                "VirtualTaskStatus": null,
                "RecycleTips": null,
                "RecycleUser": null,
                "NewOrUpdate": null,
                "Params": null,
                "TaskLinkInfo": null,
                "ImportResult": null,
                "ContentType": null,
                "TaskAutoSubmit": null,
                "ProductName": "DATA_DEV",
                "OwnId": "100028448903",
                "UserId": "100028578753",
                "TenantId": "1315051789",
                "UpdateUser": null,
                "UpdateTime": null,
                "UpdateUserId": null,
                "SchedulerDesc": null,
                "ResourceGroup": null,
                "VersionDesc": null,
                "LinkId": null,
                "UserFileId": "3a693d01-6109-4e79-a239-2d65d37e57e9",
                "Alarms": null,
                "DependencyConfigList": null,
                "ImportErrMsg": null
            }
        ]
    }
}
```

