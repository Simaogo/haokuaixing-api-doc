## 贵州好快行科技有限公司API接口

### 请求接口

**请求url:** https://******/api/etcinterface

**请求参数：**json格式

```json
{
  	"accessCode":"10A554153B4D7B558075D0BDCF630804",//商户accessCode
    "requestId":"20230606114251412053",//唯一请求ID
 	"method":"transaction/whiteListLevel",  //请求接口类型
    "data":"RuaF0uDkvprIM9LS7Lb+ndlwvWR8FM+QkTAA0244jdc=",//base64
    "sign":"72EDEDD16BEEA2FE9333A189875A7952"//签名
}
```

**sign签名**：

> accessCode**XXXXXX**`signCode`requestId**XXXXXX**signCodemethod**XXXXXX**signCodedata**XXXXXX**signCode

XXXXXX为参数值,signCode为signCode的值，可登录商户后台获取

**加密解密**：

​		参考Ddemo的加密解密方式，有php和java参考版本。



响应数据**：

```json
{
    "respCode":"0000",
    "respMessage":"操作成功",
    "responseId":"20230606113052197339",
    "data":"RuaF0uDkvprIM9LS7Lb+ndlwvWR8FM+QkTAA0244jdc="
}
```

说明：data 解密后可查看





## 1.无线交易data参数

### data值：

```json
{
    "serviceType":"2",//支付类型
    "entranceTime":"2022-08-29 10:18:41",
    "transTime":"2022-09-02 15:39:18",
    "entranceNo":"lane1",
    "parkingTimes":-559,
    "transFee":"600",
    "exportNo":"lane1",
    "vehiclePlate":"贵H7K099",
    "parkingId":"5226260025",
    "exportName":"出口",
    "extendInfo":"",
    "exportTime":"2022-08-29 12:59:03",
    "vehiclePlateColor":"0",
    "isClearingAcount":"1",
    "entranceName":"入口",
    "merchantNo":"prod_0_1565605267663228929"
 }
        
```

### method值：

transaction/noAntennaTransaction



## 2.车辆白名单查询