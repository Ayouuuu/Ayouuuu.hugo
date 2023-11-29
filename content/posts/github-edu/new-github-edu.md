---
title: "再一次通过！无EDU邮箱Github学生认证申请的艰辛历程"
date: 2023-11-06T02:48:32Z
keywords: ["Github","学生认证","Student","edu","education"]

tags:
- Github
categories:
- 总结
---

> 距 7月29日 学生认证过期后的两个月 9月26日，刚好新学校的学信网有档案了，在此期间经历了 1个多月12次申请失败，终于在10月30号申请成功。  
> 下面是我个人申请学生认证以及帮助同学申请所得出来的经验，希望能够帮助到您！

## 准备
- [Github](https://github.com) 账号
- 一台手机
  - VPN (仅代理域名 `bing.com` `google.com` )
  - 可以打开前后置摄像头
  - 位置服务
  - 虚拟定位软件 (可选)
- [学信网教育认证英文图片](https://www.chsi.com.cn/)

## 详细步骤

### 学信网认证图片
这里使用 [学信网PDF一键转换](http://www.ez4stu.nagi.fun/) 直接转换，然后做一部分修改如下图所示,修改完保存好图片，后面需要使用。
![学信网英文图片](images/chsi.webp " ")

### 修改 Github 个人信息
#### Public profile
![public profile](images/profile.webp " ")

#### Billing and plans
![billing](images/billing.webp " ")

### 申请认证
完成以上步骤后，打开[申请页面](https://education.github.com/)进行学生认证，如下图所示。  
这里我没有 `edu` 邮箱也是可以同样申请的！
![学生认证](images/step1.webp " ")

#### 位置验证
点击绿色按钮`Continue`后，一般情况下会出现`位置服务请求`，然后跳转到有`微软地图`的页面，如果不挂**代理**,可能会导致无法正常加载页面，则一直卡在`Continue`页面。挂了代理后可能会导致定位的坐标在代理的位置，这个问题`虚拟定位`可以解决。  
还有一种情况就是不会加载地图，可以直接进入[拍照环节](#拍照环节)!
![微软地图](images/step2.webp " ")
![位置信息](images/step2_1.webp " ")

`*`号为必填，其他的可不用填，定位完成后点击`Continue`就可以进行拍照环节了。

#### 拍照环节
这个环节距离认证成功只剩一步之遥了！**强烈建议使用手机拍照学信网英文图片** 画质糊一点没有关系，使用上传可能会导致无法通过！
![拍照认证](images/step3.webp " ")
至此已经完成所有步骤了，点击`Continue`耐心等待即可......

## 其他
通过 `Github` 认证之后可以直接使用 `Github` 账号登陆 [`Azure`](https://azure.microsoft.com/zh-cn/free/students) 领取微软云的学生认证，如果您以前认证过只需要再次登陆可完成续订,白嫖$100!!!

## 驳回理由汇总
下面是我12次申请经历当中被驳回的理由原因，以及解决办法。

|理由|解决办法|
|:---:|:---:|
|Attendees of this school must verify and use their academic email address.|拍照环节选择第八个类别，然后理由写上在线认证和验证码
|You are unlikely to be verified until you have completed your [GitHub user profile](https://github.com/settings/profile) with your full name exactly as it appears in your academic affiliation document plus a short bio. Please do not use a variation of your name or a nickname. Once you have updated your profile information log out and log back into GitHub before re-applying.|参考 [profile](#public-profile)
|Have you completed your [GitHub user profile](https://github.com/settings/profile) with all your relevant information, such as your full name as it appears in your image and a short bio?|参考[profile](#public-profile)
|Please select proof type 'Other' for this image.|选择 `Other` 类别
|You are unlikely to be verified until you have completed your [GitHub billing information](https://github.com/settings/billing/payment_information) with your full name exactly as it appears in your academic affiliation document. You do not have to add a payment method. You may need to log out and log back in to GitHub before re-applying.|参考[billing](#billing-and-plans)
|If your school does not provide academic email then you must enable use of your device camera to capture your image.|没有`edu`邮箱，使用学信网英文认证
|You appear not to be near any campus location for the school you have selected. Your school-provided academic affiliation document must indicate virtual learning if you are remote.Please enable the application to discover your location from the browser pop-up to provide an accurate location. If you are using a VPN, please disable it when you reapply. If you believe that the school you have applied for has incorrect information that affects your current application e.g. incorrect campus location, please select ‘My selected school has incorrect or incomplete information e.g. domains or campus location’ option when submitting a GitHub Education support ticket.|不要使用 VPN 代理 Github 相关域名
|The school you selected does not appear to have a campus location in your country. Your school-provided academic affiliation document must indicate virtual learning if you are remote. If you believe that the school you have applied for has incorrect information that affects your current application e.g. incorrect email domain, please select ‘My selected school has incorrect or incomplete information e.g. domains or campus location’ option when submitting a GitHub Education support ticket.|使用VPN代理地图的时候，建议开启虚拟定位到学校附近
|Please correct your [GitHub billing information](https://github.com/settings/billing/payment_information) with your last name exactly as it appears in your academic affiliation document.|参考 [billing](#billing-and-plans)
|If your document contains a verification code please make sure it is included in your image. If not, then please submit a different document in order to demonstrate your academic affiliation.|图片当中需要有在线验证码，建议在理由里面也带上
|Please consider using your device camera to submit academic affiliation documents. Uploaded images are more easily manipulated and are therefore less trustworthy.|使用摄像头拍照，而不是 `Upload`按钮上传
