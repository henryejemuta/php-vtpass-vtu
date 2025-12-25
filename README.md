# PHP VTpass VTU Client

[![Run Tests](https://github.com/henryejemuta/php-vtpass-vtu/actions/workflows/run-tests.yml/badge.svg)](https://github.com/henryejemuta/php-vtpass-vtu/actions/workflows/run-tests.yml)
[![Latest Stable Version](https://poser.pugx.org/henryejemuta/php-vtpass-vtu/v/stable)](https://packagist.org/packages/henryejemuta/php-vtpass-vtu)
[![Total Downloads](https://poser.pugx.org/henryejemuta/php-vtpass-vtu/downloads)](https://packagist.org/packages/henryejemuta/php-vtpass-vtu)
[![License](https://poser.pugx.org/henryejemuta/php-vtpass-vtu/license)](https://packagist.org/packages/henryejemuta/php-vtpass-vtu)
[![Quality Score](https://img.shields.io/scrutinizer/g/henryejemuta/php-vtpass-vtu.svg?style=flat-square)](https://scrutinizer-ci.com/g/henryejemuta/php-vtpass-vtu)

A PHP package for integrating with the [VTpass API](https://www.vtpass.com/documentation/). This package allows you to easily purchase airtime, data, electricity, and other services provided by VTpass.

## Installation

You can install the package via composer:

```bash
composer require henryejemuta/php-vtpass-vtu
```

## Usage

```php
use HenryEjemuta\Vtpass\Client;

// Initialize the client
// For Live Environment
$client = new Client('your-api-key', 'your-public-key', 'your-secret-key');

// For Sandbox Environment
$client = new Client('your-api-key', 'your-public-key', 'your-secret-key', [
    'sandbox' => true
]);

// Get Service Categories
$categories = $client->getServiceCategories();

// Purchase Airtime
$response = $client->purchaseAirtime('mtn', 100, '08012345678');

// Purchase Data
$response = $client->purchaseData('mtn-data', '08012345678', 'sme-month-1GB', 300);
```

## Documentation

For full API documentation, please visit the [VTpass API Documentation](https://www.vtpass.com/documentation/).

## Testing

```bash
composer test
```
