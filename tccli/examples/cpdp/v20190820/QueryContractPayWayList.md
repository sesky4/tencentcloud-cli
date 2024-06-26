**Example 1: 查询合同支付方式列表接口成功示例**

查询合同支付方式列表接口成功

Input: 

```
tccli cpdp QueryContractPayWayList --cli-unfold-argument  \
    --OpenId abc \
    --OpenKey 123
```

Output: 
```
{
    "Response": {
        "ErrCode": "0",
        "ErrMessage": "ok",
        "RequestId": "98b36609-430f-49ac-ab91-814b46f6a71e",
        "Result": [
            {
                "PaymentIcon": "xxx/Weixin.jpg",
                "PaymentId": "4",
                "PaymentInternalName": "微信支付（默认银行）",
                "PaymentName": "微信支付",
                "PaymentOptionFive": "",
                "PaymentOptionFour": "",
                "PaymentOptionNine": "微信子商户号",
                "PaymentOptionOne": "",
                "PaymentOptionOther": "",
                "PaymentOptionSeven": "",
                "PaymentOptionSix": "",
                "PaymentOptionTen": "",
                "PaymentOptionThree": "",
                "PaymentOptionTwo": "",
                "PaymentTag": "WeixinTEST",
                "PaymentType": "2,3,4"
            },
            {
                "PaymentIcon": "xxx/Alipay.jpg",
                "PaymentId": "5",
                "PaymentInternalName": "支付宝（默认银行）",
                "PaymentName": "支付宝",
                "PaymentOptionFive": "",
                "PaymentOptionFour": "",
                "PaymentOptionNine": "支付宝子商户号",
                "PaymentOptionOne": "",
                "PaymentOptionOther": "",
                "PaymentOptionSeven": "",
                "PaymentOptionSix": "",
                "PaymentOptionTen": "",
                "PaymentOptionThree": "",
                "PaymentOptionTwo": "",
                "PaymentTag": "AlipayTEST",
                "PaymentType": "2,3,4"
            },
            {
                "PaymentIcon": "xxx/Weixin.jpg",
                "PaymentId": "10",
                "PaymentInternalName": "乐刷微信",
                "PaymentName": "乐刷微信",
                "PaymentOptionFive": "",
                "PaymentOptionFour": "",
                "PaymentOptionNine": "子商户号",
                "PaymentOptionOne": "",
                "PaymentOptionOther": "",
                "PaymentOptionSeven": "",
                "PaymentOptionSix": "",
                "PaymentOptionTen": "",
                "PaymentOptionThree": "",
                "PaymentOptionTwo": "",
                "PaymentTag": "WeixinLS",
                "PaymentType": "2,3,4"
            },
            {
                "PaymentIcon": "xxx/Weixin.jpg",
                "PaymentId": "11",
                "PaymentInternalName": "乐刷支付宝",
                "PaymentName": "乐刷支付宝",
                "PaymentOptionFive": "",
                "PaymentOptionFour": "",
                "PaymentOptionNine": "",
                "PaymentOptionOne": "子商户号",
                "PaymentOptionOther": "",
                "PaymentOptionSeven": "",
                "PaymentOptionSix": "",
                "PaymentOptionTen": "",
                "PaymentOptionThree": "",
                "PaymentOptionTwo": "",
                "PaymentTag": "AlipayLS",
                "PaymentType": "2,3,4"
            },
            {
                "PaymentIcon": "xxx/Weixin.jpg",
                "PaymentId": "12",
                "PaymentInternalName": "四川农信微信支付",
                "PaymentName": "四川农信微信支付",
                "PaymentOptionFive": "",
                "PaymentOptionFour": "",
                "PaymentOptionNine": "商户号",
                "PaymentOptionOne": "",
                "PaymentOptionOther": "",
                "PaymentOptionSeven": "",
                "PaymentOptionSix": "",
                "PaymentOptionTen": "",
                "PaymentOptionThree": "地区码",
                "PaymentOptionTwo": "",
                "PaymentTag": "WeixinSCNX",
                "PaymentType": "2,3,4"
            },
            {
                "PaymentIcon": "xxx/Weixin.jpg",
                "PaymentId": "13",
                "PaymentInternalName": "陕西优惠券",
                "PaymentName": "陕西优惠券",
                "PaymentOptionFive": "",
                "PaymentOptionFour": "",
                "PaymentOptionNine": "",
                "PaymentOptionOne": "商户号",
                "PaymentOptionOther": "",
                "PaymentOptionSeven": "",
                "PaymentOptionSix": "",
                "PaymentOptionTen": "",
                "PaymentOptionThree": "",
                "PaymentOptionTwo": "终端号",
                "PaymentTag": "MbCardHZF",
                "PaymentType": "2,3,4"
            },
            {
                "PaymentIcon": "xxx/Weixin.jpg",
                "PaymentId": "14",
                "PaymentInternalName": "福建农信微信支付",
                "PaymentName": "福建农信微信支付",
                "PaymentOptionFive": "",
                "PaymentOptionFour": "",
                "PaymentOptionNine": "子商户号",
                "PaymentOptionOne": "终端号",
                "PaymentOptionOther": "",
                "PaymentOptionSeven": "",
                "PaymentOptionSix": "",
                "PaymentOptionTen": "",
                "PaymentOptionThree": "",
                "PaymentOptionTwo": "",
                "PaymentTag": "WeixinFJNX",
                "PaymentType": "2,3,4"
            },
            {
                "PaymentIcon": "xxx/Weixin.jpg",
                "PaymentId": "15",
                "PaymentInternalName": "福建浦发微信",
                "PaymentName": "福建浦发微信",
                "PaymentOptionFive": "",
                "PaymentOptionFour": "",
                "PaymentOptionNine": "商户号",
                "PaymentOptionOne": "终端编号",
                "PaymentOptionOther": "",
                "PaymentOptionSeven": "",
                "PaymentOptionSix": "",
                "PaymentOptionTen": "",
                "PaymentOptionThree": "",
                "PaymentOptionTwo": "",
                "PaymentTag": "WeixinFJPF",
                "PaymentType": "2,3,4"
            },
            {
                "PaymentIcon": "xxx/Alipay.jpg",
                "PaymentId": "16",
                "PaymentInternalName": "福建浦发支付宝",
                "PaymentName": "福建浦发支付宝",
                "PaymentOptionFive": "",
                "PaymentOptionFour": "",
                "PaymentOptionNine": "商户号",
                "PaymentOptionOne": "终端编号",
                "PaymentOptionOther": "",
                "PaymentOptionSeven": "",
                "PaymentOptionSix": "",
                "PaymentOptionTen": "",
                "PaymentOptionThree": "",
                "PaymentOptionTwo": "",
                "PaymentTag": "AlipayFJPF",
                "PaymentType": "2,3,4"
            },
            {
                "PaymentIcon": "xxx/UnionPay.jpg",
                "PaymentId": "17",
                "PaymentInternalName": "福建浦发银联",
                "PaymentName": "福建浦发银联",
                "PaymentOptionFive": "",
                "PaymentOptionFour": "",
                "PaymentOptionNine": "商户号",
                "PaymentOptionOne": "终端号",
                "PaymentOptionOther": "",
                "PaymentOptionSeven": "",
                "PaymentOptionSix": "",
                "PaymentOptionTen": "",
                "PaymentOptionThree": "",
                "PaymentOptionTwo": "",
                "PaymentTag": "UnionFJPF",
                "PaymentType": "2,3,4"
            },
            {
                "PaymentIcon": "xxx/Weixin.jpg",
                "PaymentId": "18",
                "PaymentInternalName": "烟台农信微信",
                "PaymentName": "烟台农信微信",
                "PaymentOptionFive": "",
                "PaymentOptionFour": "",
                "PaymentOptionNine": "商户号",
                "PaymentOptionOne": "",
                "PaymentOptionOther": "",
                "PaymentOptionSeven": "",
                "PaymentOptionSix": "",
                "PaymentOptionTen": "",
                "PaymentOptionThree": "机构号",
                "PaymentOptionTwo": "",
                "PaymentTag": "WeixinYTZZ",
                "PaymentType": "2,3,4"
            },
            {
                "PaymentIcon": "xxx/Weixin.jpg",
                "PaymentId": "19",
                "PaymentInternalName": "烟台支付宝",
                "PaymentName": "烟台支付宝",
                "PaymentOptionFive": "",
                "PaymentOptionFour": "",
                "PaymentOptionNine": "商户号",
                "PaymentOptionOne": "",
                "PaymentOptionOther": "",
                "PaymentOptionSeven": "",
                "PaymentOptionSix": "",
                "PaymentOptionTen": "",
                "PaymentOptionThree": "机构号",
                "PaymentOptionTwo": "",
                "PaymentTag": "AlipayYTZZ",
                "PaymentType": "2,3,4"
            },
            {
                "PaymentIcon": "xxx/Weixin.jpg",
                "PaymentId": "21",
                "PaymentInternalName": "乐刷微信(生产)",
                "PaymentName": "乐刷微信(生产)",
                "PaymentOptionFive": "",
                "PaymentOptionFour": "",
                "PaymentOptionNine": "",
                "PaymentOptionOne": "子商户号",
                "PaymentOptionOther": "",
                "PaymentOptionSeven": "",
                "PaymentOptionSix": "",
                "PaymentOptionTen": "",
                "PaymentOptionThree": "",
                "PaymentOptionTwo": "",
                "PaymentTag": "WeixinLS2",
                "PaymentType": "2,3,4"
            }
        ]
    }
}
```

