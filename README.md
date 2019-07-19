# Dnspod_API

Dnspod API Class 

The [DNSPod User API](https://www.dnspod.cn/docs/index.html) is restricted to individual users, making it easier and more flexible for users to manage their own domain names and records.

`Need to cooperate with Curl extension`

### Packagist

[![Version](http://img.shields.io/packagist/v/yakeing/dnspod_api.svg)](https://github.com/yakeing/Dnspod_API/releases)
[![Downloads](http://img.shields.io/packagist/dt/yakeing/dnspod_api.svg)](https://packagist.org/packages/yakeing/Dnspod_API)

### Github

[![Downloads](https://img.shields.io/github/downloads/yakeing/Dnspod_API/total.svg)](https://github.com/yakeing/Dnspod_API)
[![Size](https://img.shields.io/github/size/yakeing/Dnspod_API/src/dnspod.php.svg)](https://github.com/yakeing/Dnspod_API/blob/master/src/dnspod.php)
[![tag](https://img.shields.io/github/tag/yakeing/Dnspod_API.svg)](https://github.com/yakeing/Dnspod_API/releases)
[![Language](https://img.shields.io/github/license/yakeing/Dnspod_API.svg)](https://github.com/yakeing/Dnspod_API/blob/master/LICENSE)
[![Php](https://img.shields.io/github/languages/top/yakeing/Dnspod_API.svg)](https://github.com/yakeing/Dnspod_API)

### Installation

Use [Composer](https://getcomposer.org) to install the library.

```
    $ composer require yakeing/dnspod_api
```

### Initialization parameter

- [x] Sample：
```php
    $uid = 12345;
    $token = X12345;
    $DP = new Dnspod($uid, $token);
```

### Add or modify records

- [x] Sample：
```php
    $domain = 'example.com';
    $value = array(
        '255.255.255.1',
        '255.255.255.2',
        '255.255.255.3',
        );
    $name = 'www';
    $type = 'A';
    $DP->Records($domain, $value, $name, $type, true);
```

### Copy A record

- [x] Sample：
```php
    $domain = 'example.com';
    $DP->copyArecord($domain);
```

### Get domain information

- [x] Sample：
```php
    $copyDomain = 'google.com';
    $toDomain = 'example.com';
    echo $DP->getDomainInfo($copyDomain, $toDomain);
```

### Get a list of records

- [x] Sample：
```php
    $domain = 'example.com';
    echo $DP->getRecordList($domain);
```

### Get details of batch tasks

- [x] Sample：
```php
    $job_id = 'j12345';
    echo $DP->getBatchDetail($job_id);
```

### Add a single record 

- [x] Sample：
```php
    $domain = 'example.com';
    $name = 'www';
    $value = '255.255.255.0';
    $type = 'A';
    echo $DP->addRecord($domain, $name, $value, $type);
```

### Add records in bulk

- [x] Sample：
```php
    $domain_id = '12345';
    $record[0] = array('name'=>'WWW', 'type'=>'A', 'value'='255.255.255.0', 'mx'=>1);
    echo $DP->batchAddRecord($domain_id, $record);
```

### Modify record

- [x] Sample：
```php
    $domain = 'example.com';
    $record_id = 'E12345';
    $name = 'WWW2';
    $value = '255.255.255.0';
    $type = 'A';
    $mx = 1;
    echo $DP->recordModify($domain, $record_id, $name, $value, $type, $mx);
```

### Modify record

- [x] Sample：
```php
    $domain = 'example.com';
    $record_id = 'E12345';
    echo $DP->recordRemove($domain, $record_id);
```


### Other functions

- [x] Sample：
```php
    //Get the API version number
    echo $DP->getVersion();
    
    //Get the level allowed line
    $domain = 'example.com';
    echo $DP->getRecordLine($domain);
    
    //Get a list of domain names
    echo $DP->getDomainList();
    
    //Construct a new record table
    $name = 'example.com';
    $type = 'A';
    $value = '255.255.255.0';
    $DP->newRecords($name, $type, $value);
```

Donate
---
Your donation makes CODE better.

 [Bitcoin](https://btc.com/1FYbZECgs3V3zRx6P7yAu2nCDXP2DHpwt8)

 1FYbZECgs3V3zRx6P7yAu2nCDXP2DHpwt8

 ![Bitcoin](https://raw.githubusercontent.com/yakeing/Content/master/Donate/Bitcoin.png)

 WeChat

 ![WeChat](https://raw.githubusercontent.com/yakeing/Content/master/Donate/WeChat.png)

 Alipay
 
 ![Alipay](https://raw.githubusercontent.com/yakeing/Content/master/Donate/Alipay.png)

Author
---

weibo: [yakeing](https://weibo.com/yakeing)

twitter: [yakeing](https://twitter.com/yakeing)
