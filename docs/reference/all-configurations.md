---
hide:
    - toc
---
# All Configurations

Below is a table that list all configuration for this add-on.

Name | Type | Web Location | CLI Location\* | Description
---- | ---- | ------------ | ------------- | -----------
SA-AwsAssets - Lookup Gen | Saved Search | Settings > Searches reports, and alerts | savedsearches.conf | Populates the lookup file `sa_aws_assets`.
SA-AwsAssets - Lookup Cleanup | Saved Search | Settings > Searches reports, and alerts | savedsearches.conf | removes old entries from kvstore lookup: `sa_aws_assets`.
sa_aws_assets | lookup | Settings > Lookups > Lookup definitions | transforms.conf | Lookup definition for the KVstore collection `sa_aws_assets_collection`.
sa_aws_assets_collection | KVStore collection | n/a\*\* | collections.conf | KVstore configuration.
sa_aws_assets_index | Search macro | Settings > Advanced Search > Search Macros | macros.conf | Index definition for the aws index that contains the sourcetype `aws:metadata`.
sa_aws_assets_retention | Search macro | Settings > Advanced Search > Search Macros | macros.conf | The amount of time for the device not being updated before it is removed from the lookup. `default "-2d"`
identity_manager://sa_aws_assets | Asset lookup configuration | Enterprise Security > Configure > Data Enrichment > Asset and Identity Management > Asset Lookups | inputs.conf | Asset configuration lookup to load AWS assets into the asset database.

> \*CLI locations are relative to `../default`. Any update to CLI configuration files should be done in the local directory.

!!! note ""
    **If you have the [Splunk App for Lookup File Editing](https://splunkbase.splunk.com/app/263), the KVStore collection `sa_aws_assets_collection` is viewable within the Web interface.
