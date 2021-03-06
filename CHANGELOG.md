# Changelog

_This file has been auto-generated from the contents of changelog.json_

## 2.2.4

### Fix

* allow the plugin to be installed as dependency to globally installed package; previously caused every composer call to crash with class declaration conflict
* don't download the web-drivers for every project when plugin installed globally

Links: [src](https://github.com/vaimo/webdriver-binary-downloader/tree/2.2.4) [diff](https://github.com/vaimo/webdriver-binary-downloader/compare/2.2.3...2.2.4)

## 2.2.3 (2019-07-25)

### Fix

* due to the fact that download target folder was tucked away in Composer cache, odd errors and false failures were prone to happen on systems where Composer cache was shared between multiple parallel runs; change: now downloading into the config owner package (that provides download links, etc)

Links: [src](https://github.com/vaimo/webdriver-binary-downloader/tree/2.2.3) [diff](https://github.com/vaimo/webdriver-binary-downloader/compare/2.2.2...2.2.3)

## 2.2.2 (2019-06-03)

### Fix

* make downloader failure reties to be done after regular intervals (set to 2 seconds) to alleviate issues with clashes on cache cleanup
* increase downloader failure retries to 5 (used to be 2)
* parallel runs of the download for certain driver always use unique tmp paths for downloaded package (random value introduced into the generation of the cache path)

Links: [src](https://github.com/vaimo/webdriver-binary-downloader/tree/2.2.2) [diff](https://github.com/vaimo/webdriver-binary-downloader/compare/2.2.1...2.2.2)

## 2.2.1 (2019-05-03)

### Fix

* version polling did not result in console log output in some cases where executable was not found at all

Links: [src](https://github.com/vaimo/webdriver-binary-downloader/tree/2.2.1) [diff](https://github.com/vaimo/webdriver-binary-downloader/compare/2.2.0...2.2.1)

## 2.2.0 (2019-05-03)

### Feature

* output polling command and raw result when running Composer with -vvv

### Fix

* remote version polling result not validated to be a valid constraint

Links: [src](https://github.com/vaimo/webdriver-binary-downloader/tree/2.2.0) [diff](https://github.com/vaimo/webdriver-binary-downloader/compare/2.1.0...2.2.0)

## 2.1.0 (2019-05-02)

### Feature

* allow multiple version checking url's to cater for download sources that might have different mechanisms for fetching information about latest driver versions
* new path variables for having partial version in file names: major (X), major-minor (X.Y)
* retry driver download when download failed for some reason (2 retries)

### Maintenance

* introduced the use of Static Code Analysis tools
* code downgraded so to make the package installable on relatively old php versions

Links: [src](https://github.com/vaimo/webdriver-binary-downloader/tree/2.1.0) [diff](https://github.com/vaimo/webdriver-binary-downloader/compare/2.0.0...2.1.0)

## 2.0.0 (2018-12-12)

### Breaking

* (config) version polling output parser switched to use RegEx pattern matching instead of relying on sscanf

### Feature

* allow driver version polling to use version aliases (required for some drivers that use multiple versioning schemes (like EdgeDriver))
* try version polling with escaped path on Windows if normal call results in blank response

Links: [src](https://github.com/vaimo/webdriver-binary-downloader/tree/2.0.0) [diff](https://github.com/vaimo/webdriver-binary-downloader/compare/1.0.0...2.0.0)

## 1.0.0 (2018-12-12)

### Feature

* allow webdriver binary download based on passed-in configuration

Links: [src](https://github.com/vaimo/webdriver-binary-downloader/tree/1.0.0) [diff](https://github.com/vaimo/webdriver-binary-downloader/compare/7d40067f71ec830a9589bf63b6117753c1e77746...1.0.0)