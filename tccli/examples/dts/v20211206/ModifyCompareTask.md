**Example 1: 修改一致性校验任务**



Input: 

```
tccli dts ModifyCompareTask --cli-unfold-argument  \
    --JobId dts-p1sposne \
    --CompareTaskId dts-8yv4w2i1-cmp-37skmii9 \
    --TaskName test_cmp \
    --ObjectMode custom \
    --Objects.ObjectMode partial \
    --Objects.ObjectItems.0.DbName big100 \
    --Objects.ObjectItems.0.DbMode partial \
    --Objects.ObjectItems.0.TableMode partial \
    --Objects.ObjectItems.0.Tables.0.TableName sbtest1 \
    --Objects.ObjectItems.1.DbName db1 \
    --Objects.ObjectItems.1.DbMode all \
    --Objects.ObjectItems.1.TableMode all \
    --Objects.ObjectItems.1.ViewMode all
```

Output: 
```
{
    "Response": {
        "RequestId": "ac300ff0-00f2-11ed-b005-4930e69d89c2"
    }
}
```

