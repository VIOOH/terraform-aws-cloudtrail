# terraform-aws-cloudtrail

Terraform module which creates CloudTrail resources on AWS.

## Usage

### Minimal

```hcl
module "cloudtrail" {
  source         = "git::https://github.com/tmknom/terraform-aws-cloudtrail.git?ref=master"
  name           = "default-trail"
  s3_bucket_name = "cloudtrail-bucket"
}
```

## Examples

- [Minimal](https://github.com/tmknom/terraform-aws-cloudtrail/tree/master/examples/minimal)

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-----:|:-----:|
| enable_log_file_validation | Specifies whether log file integrity validation is enabled. | string | `true` | no |
| enable_logging | Enables logging for the trail. | string | `true` | no |
| include_global_service_events | Specifies whether the trail is publishing events from global services such as IAM to the log files. | string | `true` | no |
| is_multi_region_trail | Specifies whether the trail is created in the current region or in all regions. | string | `true` | no |
| name | Specifies the name of the trail. | string | - | yes |
| s3_bucket_name | Specifies the name of the S3 bucket designated for publishing log files. | string | - | yes |

## Outputs

| Name | Description |
|------|-------------|
| cloudtrail_arn | The Amazon Resource Name of the trail. |
| cloudtrail_home_region | The region in which the trail was created. |
| cloudtrail_name | The name of the trail. |

## License

Apache 2 Licensed. See LICENSE for full details.
