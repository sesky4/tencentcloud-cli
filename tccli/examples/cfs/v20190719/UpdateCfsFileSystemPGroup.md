**Example 1: Updating the permission group for a file system**



Input: 

```
tccli cfs UpdateCfsFileSystemPGroup --cli-unfold-argument  \
    --FileSystemId cfs-12345 \
    --PGroupId pgroup-12345
```

Output: 
```
{
    "Response": {
        "RequestId": "fjo8aejo-fjei-32eu-2je9-fhue83nd81",
        "PGroupId": "pgroup-12345",
        "FileSystemId": "cfs-12345"
    }
}
```
