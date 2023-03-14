# Troubleshooting

There can be many issues when setting up a new app/add-on in Splunk. Below highlights the most common issues with this Add-on. Don't see your issue? Submit a new issue on [GitHub](https://github.com/ZachChristensen28/SA-AwsAssets/issues){ target=blank }.

Issue | Description | Solution
----- | ----------- | --------
Multiple asset merge | It is possible that some of your devices share a common mac address or another key field which will cause merging by default. | If Aws is your only asset source you can disable asset merge under global settings. See [Asset Merge Solution](./solution-guides/asset-merge) for more information.
Asset Database not populating with Aws Data | The asset database may show no Aws data if the initial search has not run to build the asset database or the default macro has not been updated. | Verify the default macro has the correct index definition (see [Update Default Macro](/quickstart/quickstart/#update-default-macro)). Also see [Force build](/quickstart/quickstart/#force-initial-build) to build the Aws assets lookup before the first scheduled run.
Lookup file error | You may see the error `status="Lookup file error, unknown path or update time" name=sa_aws_assets` | This error exists since the KVstore is being used opposed to a csv file and does not interfere with the functionality of lookup creation.
Empty IP/MAC address fields | If you see empty IP/MAC fields for some instances, this could be related to [issue #20 on GitHub](https://github.com/ZachChristensen28/SA-AwsAssets/issues/20){ target=blank }. With multiple interfaces IP/MAC address fields did not extract correctly. | Upgrade to the latest version for fix (version >= 1.0.3).
