# Release notes

## [v1.0.2 <small>December 20, 2022</small>](https://github.com/ZachChristensen28/SA-AwsAssets/releases/tag/v1.0.2)

### Compatibility

Product | Version
--------- | -------
Splunk platform versions | 9.x, 8.x
Splunk Enterprise Security version | [7.x, 6.x](https://splunkbase.splunk.com/app/263)
Splunk Add-on for AWS | [6.x](https://splunkbase.splunk.com/app/1876)

### What's Changed

- Added macro and retention definition to ES General Settings in [#10](https://github.com/ZachChristensen28/SA-AwsAssets/commit/26505484080f244afe6c52b7f59bf8963fc5a607)

**Full Changelog**: [v1.0.1...v1.0.2](https://github.com/ZachChristensen28/SA-AwsAssets/compare/v1.0.1...v1.0.2)

## Known issues

Issue | Description | Solution | GitHub issue reference
----- | ----------- | -------- | ----------------------
Lookup file error | You may see the error `status="Lookup file error, unknown path or update time" name=sa_aws_assets` | This error exists since the KVstore is being used opposed to a csv file and does not interfere with the functionality of lookup creation. | Issue [#1](https://github.com/ZachChristensen28/SA-AwsAssets/issues/1){ target=blank }
Multiple network interfaces with no IP/MAC | EC2 instances with multiple network interfaces do not get their ip and mac address fields rendered correctly in that they are treated as mv fields rather than a pipe-concatenated string. | Upgrade to latest release (when available) | Issue [#20](https://github.com/ZachChristensen28/SA-AwsAssets/issues/20){ target=blank }

Issues can be reported on the [SA-AwsAssets's Github page](https://github.com/ZachChristensen28/SA-AwsAssets/issues).
