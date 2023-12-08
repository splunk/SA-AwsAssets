# Asset Database Mapping

The following table describes how this add-on maps to the Asset Database.

> reference [Format an asset or identity in Splunk Enterprise Security <small>:icon-link-external:</small>](https://docs.splunk.com/Documentation/ES/latest/Admin/Formatassetoridentitylist#Asset_lookup_header){ target="blank" }

ES Asset lookup field | `aws:metadata` sourcetype fields | Example value | Multivalue allowed
--- | --- | --- | ---
ip | `NetworkInterfaces{}.PrivateIpAddress` | 10.15.23.8 | true
mac | `NetworkInterfaces{}.MacAddress` | `61:se:e3:1s:7r:38` | true
nt_host | `NetworkInterfaces{}.Association.PublicDnsName` + `NetworkInterfaces{}.PrivateDnsName` + `NetworkInterfaces{}.PrivateIpAddresses{}.Association.PublicDnsName` | dev-server01 | false
dns | `dns` | dev-server01.example.com | true
owner | n/a | `not mapped`| n/a
priority | see [Configure Priority](/configure/priority.md) | medium | false
lat | from `iplocation` of `NetworkInterfaces{}.Association.PublicIp` | 40.76073 | false
long | from `iplocation` of `NetworkInterfaces{}.Association.PublicIp` | -111.89096 | false
city | from `iplocation` of `NetworkInterfaces{}.Association.PublicIp` | Salt Lake City | false
country | from `iplocation` of `NetworkInterfaces{}.Association.PublicIp` | United States | false
bunit | n/a | `not mapped` | true
category | see [Category field reference](category.md) | see [Category field reference](category.md) | true
pci_domain | n/a | `not mapped` | n/a
is_expected | n/a | `not mapped` | n/a
should_timesync | n/a | `not mapped` | n/a
should_update | n/a | `not mapped` | n/a
requires_av | n/a | `not mapped` | n/a
cim_entity_zone | n/a | `not mapped` | n/a
