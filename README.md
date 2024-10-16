﻿# 💾 VPNResellers PHP API Client

![visitors](https://visitor-badge.laobi.icu/badge?page_id=exbil.vpnresellers-php-api)
![](https://img.shields.io/badge/stable-v.1.0-informational?style=flat&logoColor=white&color=6aa6f8)
![](https://img.shields.io/badge/license-MIT-informational?style=flat&logoColor=white&color=6aa6f8)

### This GitHub Repo was Developed by Julien Michell Herwig (Vexura) [Orginal Files](https://github.com/Vexura/vpnresellers-api/)

# Getting Started
### Requirements
* [**PHP 7.4+**](https://www.php.net/downloads.php)
* Extensions: [Composer](https://getcomposer.org/), [PHP-JSON](https://www.php.net/manual/en/book.json.php)

# ⚒️ Install
In the root of your project execute the following:
```sh
composer require exbil/vpnresellers-php-api
```
or add this to your `composer.json` file:
```json
{
  "require": {
    "exbil/vpnresellers-php-api": "^1.0"
  }
}
```

Then perform the installation:
```sh
$ composer install --no-dev
```

# 📑 Usage

Search for the official API Documentation [here](https://api.vpnresellers.com/docs/v3_1).  
You need an [API Key](https://app.vpnresellers.com/api-access) for that.

### 🗃️ Basic

```php
<?php
// Require the autoloader
require_once 'vendor/autoload.php';
// Use the library namespace
use VPNResellersAPI\VPNResellersAPI;
// Then simply pass your API-Token when creating the API client object.
$apiKey = getenv('VPNRESELLERS_API_KEY');
$client = new VPNResellersAPI($apiKey);
// Then you are able to perform a request
var_dump($client->servers()->getServers());
?>
```
