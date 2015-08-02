# Breezometer php

[![Latest Version](https://img.shields.io/github/release/nwidart/forecast-php.svg?style=flat-square)](https://github.com/nwidart/forecast-php/releases)
[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE.md)
[![Build Status](https://img.shields.io/travis/nwidart/forecast-php/master.svg?style=flat-square)](https://travis-ci.org/nwidart/forecast-php)
[![Coverage Status](https://img.shields.io/scrutinizer/coverage/g/nwidart/forecast-php.svg?style=flat-square)](https://scrutinizer-ci.com/g/nwidart/forecast-php/code-structure)
[![Quality Score](https://img.shields.io/scrutinizer/g/nwidart/forecast-php.svg?style=flat-square)](https://scrutinizer-ci.com/g/nwidart/forecast-php)
[![Total Downloads](https://img.shields.io/packagist/dt/addapp/forecast-php.svg?style=flat-square)](https://packagist.org/packages/addapp/forecast-php)

A PHP client package for the [Forecast.io](https://forecast.io/) [API](https://developer.forecast.io/).

Want to use this inside a Laravel application? Check out the [Laravel-Forecast](https://github.com/nWidart/Laravel-forecast) package.

## Install

Via Composer

``` bash
$ composer require nwidart/forecast-php
```

## Usage

``` php
$forecast = new \Nwidart\ForecastPhp\Forecast('your_api_key');

$info = $forecast->get('40.7324296', '-73.9977264');
```

Will return something like :

``` json
{
  "latitude": 40.7324296,
  "longitude": -73.9977264,
  "timezone": "America/New_York",
  "offset": -4,
  "currently": {
    "time": 1438445386,
    "summary": "Partly Cloudy",
    "icon": "partly-cloudy-day",
    "nearestStormDistance": 63,
    "nearestStormBearing": 360,
    "precipIntensity": 0,
    "precipProbability": 0,
    "temperature": 84.71,
    "apparentTemperature": 85.39,
    "dewPoint": 62.25,
    "humidity": 0.47,
    "windSpeed": 7.95,
    "visibility": 10,
    "cloudCover": 0.59,
    "pressure": 1010.33,
    "ozone": 323.24
  },
  "minutely": {
    ...
  },
  "hourly": {
    ...
  },
  "daily": {
    ...
  },
  "flags": {
    ...
  },
  "headers": {
    ...
  }
}
```

## Testing

``` bash
$ phpunit
```

## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) for details.

## Credits

- [Nicolas Widart](https://github.com/nWidart)
- [All Contributors](../../contributors)

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
