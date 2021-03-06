# Chronopost API

A PHP package to make the Chronopost API easier to use.

## Table of Contents

* [Requirements](#requirements)  
* [Installation](#installation)
* [Usage](#usage)
* [Testing](#testing)

## Requirements

* PHP 7.3, 8.0 or 9.0

## Installation

```
composer require kozennnn/chronopost-api
```

## Usage

The following code return all the available Chronopost Pickup points.

```php
<?php

use Kozennnn\ChronopostAPI\ChronopostAPI;

$chronopost = new ChronopostAPI();
print_r($chronopost->getPickupPointsFromZipCode('44000')); // will print array with all the pickup points

```
#

The following code return the package tracking informations.

```php
<?php

use Kozennnn\ChronopostAPI\ChronopostAPI;

$chronopost = new ChronopostAPI();
print_r($chronopost->trackPackage('FD633119313NZ')); // will print array with the package tracking informations.

```

## Testing

```
php tests/ChronopostAPITest.php
```