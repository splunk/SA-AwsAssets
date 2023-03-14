# Release notes

## [v1.0.3 <small>March 13, 2023</small>](https://github.com/ZachChristensen28/SA-AwsAssets/releases/tag/v1.0.3){ target=blank }

### Compatibility

Product | Version
------- | -------
Splunk platform versions | 9.x, 8.x
Splunk Enterprise Security version | [7.x, 6.x](https://splunkbase.splunk.com/app/263){ target=blank }
Splunk Add-on for AWS | [6.x](https://splunkbase.splunk.com/app/1876){ target=blank }

### What's Changed

- Fixed empty IP/MAC address for instances with multiple interfaces - [#20](https://github.com/ZachChristensen28/SA-AwsAssets/issues/20){ target=blank } Thanks [@barrettnet](https://github.com/barrettnet){ target=blank }

**Full Changelog**: [v1.0.2...v1.0.3](https://github.com/ZachChristensen28/SA-AwsAssets/compare/v1.0.2...v1.0.3){ target=blank }

## Known issues

Issue | Description | Solution | GitHub issue reference
----- | ----------- | -------- | ----------------------
Lookup file error | You may see the error `status="Lookup file error, unknown path or update time" name=sa_aws_assets` | This error exists since the KVstore is being used opposed to a csv file and does not interfere with the functionality of lookup creation. | Issue [#1](https://github.com/ZachChristensen28/SA-AwsAssets/issues/1){ target=blank }

Issues can be reported on the [SA-AwsAssets's Github page](https://github.com/ZachChristensen28/SA-AwsAssets/issues){ target=blank }.
