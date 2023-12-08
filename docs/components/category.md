# Category Field

## Default category field mapping

Mapped Field | sourcetype=aws:metadata Event Field | Example value
------------ | ----------------------- | -------------
availability_zone | `Placement.AvailabilityZone` | us-east-1d
enabled | `enabled` | true
group_id | `SecurityGroups{}.GroupId` | sg-934752093485034
group_name | `SecurityGroups{}.GroupName` | webserver
hypervisor | `Hypervisor` | xen
image_id | `ImageId` | ami-83477fed042321
instance_type | `InstanceType` | t2.micro
launch_time | `LaunchTime` | 10/28/22 19:04:38 utc
monitoring | `Monitoring.State` | disabled
public_ip | `NetworkInterfaces{}.Association.PublicIp` | 0.0.0.0
region | `Region` | us-east-1
state | `State.Name` | running
subnet_id | `NetworkInterfaces{}.SubnetId` | subnet-8394d882
tags | `custom_tag` | dev web server
vpc_id | `NetworkInterfaces{}.VpcId` | vpc-0c38d38eae842145
splunk_last_updated | `now()` | 09/29/22 18:55:51 mdt

### Full example of category value

```yaml
availability_zone: us-east-1d
enabled: true
gen: sa-aws-assets
group_id: sg-046036e7384042b7
group_name: webserver
hypervisor: xen
image_id: ami-0c02fb53sd46c7d316
instance_type: t2.medium
launch_time: 10/28/22 19:04:38 utc
monitoring: disabled
public_ip: 0.0.0.0
region: ec2_instances
splunk_last_updated: 10/28/22 20:21:39 utc
state: running
subnet_id: subnet-0c08bkd3ae32c536b
tags: name:web server
vpc_id: vpc-0c835c7sx3dsrca4f8
```