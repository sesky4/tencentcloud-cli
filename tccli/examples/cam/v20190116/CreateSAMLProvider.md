**Example 1: 创建身份提供商**



Input: 

```
tccli cam CreateSAMLProvider --cli-unfold-argument  \
    --Name testName \
    --Description testProvider \
    --SAMLMetadataDocument PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiPz48bWQ6RW50aXR5RGVzY3JpcHRvciBlbnRpdHlJRD0iaHR0cDovL3d3dy5va3RhLmNvbS9leGsxa3F4bWNqUW1HQURNeTM1NyIgeG1sbnM6bWQ9InVybjpvYXNpczpuYW1lczp0YzpTQU1MOjIuMDptZXRhZGF0YSI%2BPG1kOklEUFNTT0Rlc2NyaXB0b3IgV2FudEF1dGhuUmVxdWVzdHNTaWduZWQ9ImZhbHNlIiBwcm90b2NvbFN1cHBvcnRFbnVtZXJhdGlvbj0idXJuOm9hc2lzOm5hbWVzOnRjOlNBTUw6Mi4wOnB%3D%3D
```

Output: 
```
{
    "Response": {
        "ProviderArn": "testProviderArn",
        "RequestId": "2a44e8e5-7438-4aa0-8bd2-584dde56caab"
    }
}
```

