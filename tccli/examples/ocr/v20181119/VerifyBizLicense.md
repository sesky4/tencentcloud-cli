**Example 1: 营业执照识别及核验详细版示例代码（使用图片进行核验）**

营业执照识别及核验详细版示例代码（使用图片进行核验）

Input: 

```
tccli ocr VerifyBizLicense --cli-unfold-argument  \
    --ImageUrl https://xx/a.jpg \
    --ImageConfig {"RegNum":true,"Name":true,"Address":true}
```

Output: 
```
{
    "Response": {
        "ErrorCode": 0,
        "CreditCode": "911101085636549482",
        "OrgCode": "563654948",
        "OpenFrom": "2010-10-21",
        "OpenTo": "2030-10-20",
        "FrName": "谢兰芳",
        "EnterpriseStatus": "在营（开业）",
        "OperateScopeAndForm": "利用互联网经营游戏产品运营、网络游戏虚拟货币发行、从事互联网文化产品的展览、比赛活动；经营电信业务（以增值电信业务经营许可证核定范围为准）（增值电信业务经营许可证有效期至2023年11月28日）；人力资源服务；销售第三类医疗器械；专利代理；技术开发、技术转让、技术咨询；设计、制作、代理、发布广告；基础软件服务；应用软件服务；销售自行开发的产品、医疗器械I类、II类、计算机、软件及辅助设备、通讯设备、机械设备、电子产品；货物进出口、技术进出口、代理进出口；企业管理咨询；市场调查；商标代理；著作权代理服务；移动电信、宽带网络的技术服务；代理记账。（企业依法自主选择经营项目，开展经营活动；代理记账以及依法须经批准的项目，经相关部门批准后依批准的内容开展经营活动；不得从事本市产业政策禁止和限制类项目的经营活动。）",
        "RegCap": "14250.00",
        "RegCapCur": "人民币",
        "RegOrg": "北京市工商行政管理局海淀分局",
        "EsDate": "2010-10-21",
        "EnterpriseType": "其他有限责任公司",
        "CancelDate": "",
        "RevokeDate": "",
        "AbuItem": "",
        "CbuItem": "",
        "ApprDate": "2019-11-20",
        "Province": "北京",
        "City": "北京市",
        "County": "海淀区",
        "AreaCode": "110108",
        "IndustryPhyCode": "I",
        "IndustryPhyName": "信息传输、软件和信息技术服务业",
        "IndustryCode": "6439",
        "IndustryName": "其他互联网平台",
        "OperateScope": "利用互联网经营游戏产品运营、网络游戏虚拟货币发行、从事互联网文化产品的展览、比赛活动；经营电信业务（以增值电信业务经营许可证核定范围为准）（增值电信业务经营许可证有效期至2023年11月28日）；人力资源服务；销售第三类医疗器械；专利代理；技术开发、技术转让、技术咨询；设计、制作、代理、发布广告；基础软件服务；应用软件服务；销售自行开发的产品、医疗器械I类、II类、计算机、软件及辅助设备、通讯设备、机械设备、电子产品；货物进出口、技术进出口、代理进出口；企业管理咨询；市场调查；商标代理；著作权代理服务；移动电信、宽带网络的技术服务；代理记账。（企业依法自主选择经营项目，开展经营活动；代理记账以及依法须经批准的项目，经相关部门批准后依批准的内容开展经营活动；不得从事本市产业政策禁止和限制类项目的经营活动。）",
        "VerifyRegNo": "911101085636549482",
        "RegNo": "110108013297537",
        "VerifyEnterpriseName": "腾讯云计算(北京)有限责任公司",
        "EnterpriseName": "腾讯云计算（北京）有限责任公司",
        "VerifyAddress": "北京市海淀区知春路49号3层西部309",
        "Address": "北京市海淀区知春路49号3层西部309",
        "RegNumResult": {
            "RegNum": "0",
            "Name": "-1",
            "Address": "0"
        },
        "RequestId": "3ec63378-af53-4b26-babc-4dbb63c84716"
    }
}
```

**Example 2: 营业执照识别及核验详细版示例代码（输入关键字段进行核验）**

营业执照识别及核验详细版示例代码（输入关键字段进行核验）

Input: 

```
tccli ocr VerifyBizLicense --cli-unfold-argument  \
    --RegNum 911101085636549482 \
    --Name 腾讯云计算（北京）有限责任公司 \
    --Address 北京市海淀区知春路49号3层西部309
```

Output: 
```
{
    "Response": {
        "AbuItem": "",
        "Address": "北京市海淀区西北旺东路10号院西区9号楼4层101",
        "ApprDate": "2023-01-17",
        "AreaCode": "",
        "CancelDate": "",
        "CbuItem": "",
        "City": "北京市",
        "County": "海淀区",
        "CreditCode": "911101085636549482",
        "EnterpriseName": "腾讯云计算（北京）有限责任公司",
        "EnterpriseStatus": "存续",
        "EnterpriseType": "有限责任公司(法人独资)",
        "ErrorCode": 0,
        "EsDate": "2010-10-21",
        "FrName": "谢兰芳",
        "IndustryCode": "",
        "IndustryName": "",
        "IndustryPhyCode": "",
        "IndustryPhyName": "",
        "OpenFrom": "2010-10-21",
        "OpenTo": "2030-10-20",
        "OperateScope": "",
        "OperateScopeAndForm": "利用互联网经营游戏产品运营、网络游戏虚拟货币发行、从事互联网文化产品的展览、比赛活动；经营电信业务（以增值电信业务经营许可证核定范围为准）（增值电信业务经营许可证有效期至2023年11月28日）；人力资源服务；销售第三类医疗器械；专利代理；技术开发、技术转让、技术咨询；设计、制作、代理、发布广告；基础软件服务；应用软件服务；销售自行开发的产品、医疗器械I类、II类、计算机、软件及辅助设备、通讯设备、机械设备、电子产品；货物进出口、技术进出口、代理进出口；企业管理咨询；市场调查；商标代理；著作权代理服务；移动电信、宽带网络的技术服务；代理记账。（市场主体依法自主选择经营项目，开展经营活动；代理记账以及依法须经批准的项目，经相关部门批准后依批准的内容开展经营活动；不得从事国家和本市产业政策禁止和限制类项目的经营活动。）",
        "OrgCode": "563654948",
        "Province": "北京",
        "RegCap": "",
        "RegCapCur": "",
        "RegNo": "110108013297537",
        "RegNumResult": {
            "Address": "-1",
            "Name": "0",
            "RegNum": "0"
        },
        "RegOrg": "",
        "RequestId": "e2aba233-f200-4234-807f-fd12b1a6649c",
        "RevokeDate": "",
        "VerifyAddress": "北京市海淀区知春路49号3层西部309",
        "VerifyEnterpriseName": "腾讯云计算（北京）有限责任公司",
        "VerifyRegNo": "911101085636549482"
    }
}
```

