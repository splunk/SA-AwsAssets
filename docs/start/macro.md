---
order: -3
label: Update Index
icon: command-palette
---

# Update Splunk Index

!!!danger [Danger, Will Robinson <small>:icon-link-external:</small>](https://cultural-phenomenons.fandom.com/wiki/Danger,_Will_Robinson){ target="blank" }
Failure to update the index to the correct setting will cause no devices to be available in Splunk Enterprise Security.
!!!

The index definition is set by a search macro. 

Macro | Default | Description
----- | ------- | -----------
sa_aws_assets_index | index=\`aws-index-value\` | Index definition for AWS metadata index (`sourcetype=aws:metadata`).

!!!
The `aws-index-value` search macro is included with Splunk Enterprise Security and is set to aws_security by default.
!!!

## How to update

==- :icon-star-fill: Use Splunk Enterprise Security's Settings <small>(Recommended)</small>
1. <small>(In Splunk Enterprise Security)</small> Navigate to Configure > General > General Settings.
2. From the "App" dropdown select `SA-AwsAssets`.
3. Update the SA-AwsAssets Index definition and click "Save."
==- Update Search Macro Manually
1. Navigate to Settings > Advanced Search > Search Macros.
2. From the "App" dropdown choose `SA-AwsAssets`.
3. Set the "Owner" dropdown to `any`.
4. Click the macro named `sa_aws_assets_index` to update the index definition.
===