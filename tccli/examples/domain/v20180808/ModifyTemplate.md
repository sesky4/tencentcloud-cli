**Example 1: 修改模板**



Input: 

```
tccli domain ModifyTemplate --cli-unfold-argument  \
    --TemplateId 字符串 \
    --CertificateInfo.CertificateCode 字符串 \
    --CertificateInfo.CertificateType 字符串 \
    --CertificateInfo.ImgUrl 字符串 \
    --ContactInfo.OrganizationNameCN 字符串 \
    --ContactInfo.OrganizationName 字符串 \
    --ContactInfo.RegistrantNameCN 字符串 \
    --ContactInfo.RegistrantName 字符串 \
    --ContactInfo.ProvinceCN 字符串 \
    --ContactInfo.Province 字符串 \
    --ContactInfo.CityCN 字符串 \
    --ContactInfo.City 字符串 \
    --ContactInfo.StreetCN 字符串 \
    --ContactInfo.Street 字符串 \
    --ContactInfo.CountryCN 字符串 \
    --ContactInfo.Country 字符串 \
    --ContactInfo.Telephone 字符串 \
    --ContactInfo.Email 字符串 \
    --ContactInfo.ZipCode 字符串 \
    --ContactInfo.RegistrantType 字符串
```

Output: 
```
{
    "Response": {
        "RequestId": "c9308288-****-baf0a9ea0a6f",
        "Template": {
            "IsBlack": false,
            "AuditReason": "",
            "IsValidTemplate": 1,
            "UpdatedOn": "2020-07-30 16:44:04",
            "AuditStatus": "InAudit",
            "CreatedOn": "2020-07-30 16:44:04",
            "InvalidReason": "",
            "CertificateInfo": {
                "CertificateType": "YYZZ",
                "CertificateCode": "4****075",
                "ImgUrl": "image.jpg",
                "OriginImgUrl": "image.jpg",
                "RegistrantCertificateType": "",
                "RegistrantCertificateCode": "",
                "RegistrantImgUrl": ""
            },
            "TemplateId": "tmpl-3mm9fxug",
            "UserUin": "1213059621",
            "ContactInfo": {
                "Province": "shen zhen shi",
                "RegistrantType": "E",
                "OrganizationName": "qiyeming",
                "OrganizationNameCN": "企业名",
                "Country": "CN",
                "RegistrantName": "qiyeming",
                "ZipCode": "100011",
                "Email": "121****@qq.com",
                "City": "nan shan qu",
                "RegistrantNameCN": "企业名",
                "StreetCN": "*大厦",
                "Street": "*sha",
                "ProvinceCN": "*市",
                "CountryCN": "中国",
                "CityCN": "*区",
                "Telephone": "13****2"
            },
            "IsDefault": "no"
        }
    }
}
```

