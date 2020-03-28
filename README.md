# IDENTITY-CARD
分析中国身份证的扩展包

## 安装
```shell
$ composer require chenxb/identity-card -vvv
```

## 配置
暂无配置

## 使用
```php
<?php

use Chenxb\IdentityCard\IdentityCard;

// 只检查身份证
IdentityCard::check("xxxxxxxxxxxxxxxxxxxxx");

// 检查身份证 & 并且分析身份信息
$idCardObject = IdentityCard::make('xxxxxxxxxxxxxxxxxx', 'zh-cn');
$idCardObject->getArea();  //获取获取身份证所在省市县
$idCardObject->getProvince();   // 获取省份
$idCardObject->getCity(); // 获取城市
$idCardObject->getCounty(); // 获取城市
$idCardObject->getAge(); // 获取年龄
$idCardObject->getBirthDay($format = 'Y-m-d'); // 获取生日
$idCardObject->getZodiac(); // 获取生效
$idCardObject->getGender(); // 获取性别
$idCardObject->getConstellation(); // 获取星座
$idCardObject->toArray(); // 转成数组输出
$idCardObject->toJson(); // 转成json字符串
```