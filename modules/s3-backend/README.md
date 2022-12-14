## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 1.0 |
| <a name="requirement_aws"></a> [aws](#requirement\_aws) | 4.45.0 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aws"></a> [aws](#provider\_aws) | 4.45.0 |
| <a name="provider_random"></a> [random](#provider\_random) | n/a |

## Modules

No modules.

## Resources

| Name | Type |
|------|------|
| [aws_dynamodb_table.tf_remote_state_lock](https://registry.terraform.io/providers/hashicorp/aws/4.45.0/docs/resources/dynamodb_table) | resource |
| [aws_s3_bucket.tf_remote_state](https://registry.terraform.io/providers/hashicorp/aws/4.45.0/docs/resources/s3_bucket) | resource |
| [aws_s3_bucket_server_side_encryption_configuration.mybackend](https://registry.terraform.io/providers/hashicorp/aws/4.45.0/docs/resources/s3_bucket_server_side_encryption_configuration) | resource |
| [aws_s3_bucket_versioning.versioning_backend_s3](https://registry.terraform.io/providers/hashicorp/aws/4.45.0/docs/resources/s3_bucket_versioning) | resource |
| [random_string.random](https://registry.terraform.io/providers/hashicorp/random/latest/docs/resources/string) | resource |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_backend_s3_key"></a> [backend\_s3\_key](#input\_backend\_s3\_key) | The Terraform state is written to the key | `string` | `"env/dev/tf_remote_backend.tfstate"` | no |
| <a name="input_bucket_name"></a> [bucket\_name](#input\_bucket\_name) | The name of the backend-s3 bucket | `string` | `"tf_s3_bucket_backend_task"` | no |
| <a name="input_dynamodb_table"></a> [dynamodb\_table](#input\_dynamodb\_table) | To enable locking | `string` | `"tf_s3_app_lock"` | no |
| <a name="input_sse_algorithm"></a> [sse\_algorithm](#input\_sse\_algorithm) | The server-side encryption algorithm to use. `AES256` or `aws:kms` | `string` | `"AES256"` | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_dynamodb_table"></a> [dynamodb\_table](#output\_dynamodb\_table) | n/a |
| <a name="output_s3_backend_name"></a> [s3\_backend\_name](#output\_s3\_backend\_name) | n/a |
