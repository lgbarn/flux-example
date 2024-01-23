## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >=1.2.0 |
| <a name="requirement_aws"></a> [aws](#requirement\_aws) | ~> 5.14 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aws"></a> [aws](#provider\_aws) | 5.19.0 |
| <a name="provider_random"></a> [random](#provider\_random) | 3.6.0 |

## Modules

| Name | Source | Version |
|------|--------|---------|
| <a name="module_rds-postgres-mda"></a> [rds-postgres-mda](#module\_rds-postgres-mda) | gitlab.com/polestardefense/psd-base-rds-postgres-module/aws | 1.3.1 |

## Resources

| Name | Type |
|------|------|
| [random_id.this](https://registry.terraform.io/providers/hashicorp/random/latest/docs/resources/id) | resource |
| [aws_eks_cluster.selected](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/eks_cluster) | data source |
| [aws_eks_cluster_auth.selected](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/eks_cluster_auth) | data source |
| [aws_iam_openid_connect_provider.selected](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/iam_openid_connect_provider) | data source |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_cluster_name"></a> [cluster\_name](#input\_cluster\_name) | The name of the EKS cluster. | `string` | `"eks-cluster"` | no |
| <a name="input_default_tags"></a> [default\_tags](#input\_default\_tags) | The default tags to apply to all AWS resources. | `map(string)` | n/a | yes |
| <a name="input_profile"></a> [profile](#input\_profile) | The AWS profile to use. | `string` | n/a | yes |
| <a name="input_rds_instance_class"></a> [rds\_instance\_class](#input\_rds\_instance\_class) | The RDS instance class to use. | `string` | `"db.t3.micro"` | no |
| <a name="input_rds_postgres_allocated_storage"></a> [rds\_postgres\_allocated\_storage](#input\_rds\_postgres\_allocated\_storage) | The allocated storage for the RDS Postgres instance. | `number` | `20` | no |
| <a name="input_rds_postgres_db_name"></a> [rds\_postgres\_db\_name](#input\_rds\_postgres\_db\_name) | The name of the RDS Postgres database. | `string` | `"postgres"` | no |
| <a name="input_rds_postgres_egress_cidr"></a> [rds\_postgres\_egress\_cidr](#input\_rds\_postgres\_egress\_cidr) | The egress CIDR blocks for the RDS Postgres instance. | `list(string)` | <pre>[<br>  "10.0.0.0/16"<br>]</pre> | no |
| <a name="input_rds_postgres_engine_version"></a> [rds\_postgres\_engine\_version](#input\_rds\_postgres\_engine\_version) | The engine version for the RDS Postgres instance. | `string` | `"12.5"` | no |
| <a name="input_rds_postgres_existing_vpc_id"></a> [rds\_postgres\_existing\_vpc\_id](#input\_rds\_postgres\_existing\_vpc\_id) | The existing VPC endpoint ID for the RDS Postgres instance. | `string` | `""` | no |
| <a name="input_rds_postgres_ingress_cidr"></a> [rds\_postgres\_ingress\_cidr](#input\_rds\_postgres\_ingress\_cidr) | The ingress CIDR blocks for the RDS Postgres instance. | `list(string)` | <pre>[<br>  "10.0.0.0/16"<br>]</pre> | no |
| <a name="input_rds_postgres_iops"></a> [rds\_postgres\_iops](#input\_rds\_postgres\_iops) | The IOPS for the RDS Postgres instance. | `number` | `0` | no |
| <a name="input_rds_postgres_name"></a> [rds\_postgres\_name](#input\_rds\_postgres\_name) | The name of the RDS Postgres instance. | `string` | `"postgres"` | no |
| <a name="input_rds_postgres_password"></a> [rds\_postgres\_password](#input\_rds\_postgres\_password) | The password for the RDS Postgres instance. | `string` | `"postgres"` | no |
| <a name="input_rds_postgres_port"></a> [rds\_postgres\_port](#input\_rds\_postgres\_port) | The port for the RDS Postgres instance. | `number` | `5432` | no |
| <a name="input_rds_postgres_private_subnet_ids"></a> [rds\_postgres\_private\_subnet\_ids](#input\_rds\_postgres\_private\_subnet\_ids) | The private subnet IDs for the RDS Postgres instance. | `list(string)` | `[]` | no |
| <a name="input_rds_postgres_snapshot_identifier"></a> [rds\_postgres\_snapshot\_identifier](#input\_rds\_postgres\_snapshot\_identifier) | The snapshot identifier for the RDS Postgres instance. | `string` | `""` | no |
| <a name="input_rds_postgres_storage_type"></a> [rds\_postgres\_storage\_type](#input\_rds\_postgres\_storage\_type) | The storage type for the RDS Postgres instance. | `string` | `"gp2"` | no |
| <a name="input_rds_postgres_username"></a> [rds\_postgres\_username](#input\_rds\_postgres\_username) | The username for the RDS Postgres instance. | `string` | `"postgres"` | no |
| <a name="input_region"></a> [region](#input\_region) | The AWS region to use. | `string` | `"us-gov-east-1"` | no |

## Outputs

No outputs.
<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >=1.2.0 |
| <a name="requirement_aws"></a> [aws](#requirement\_aws) | ~> 5.14 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aws"></a> [aws](#provider\_aws) | ~> 5.14 |

## Modules

| Name | Source | Version |
|------|--------|---------|
| <a name="module_rds_postgres_mda"></a> [rds\_postgres\_mda](#module\_rds\_postgres\_mda) | terraform-aws-modules/rds/aws | 6.3.1 |

## Resources

| Name | Type |
|------|------|
| [aws_security_group.rds](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/security_group) | resource |
| [aws_subnets.private](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/subnets) | data source |
| [aws_vpc.selected](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/vpc) | data source |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_default_tags"></a> [default\_tags](#input\_default\_tags) | The default tags to apply to all AWS resources. | `map(string)` | n/a | yes |
| <a name="input_profile"></a> [profile](#input\_profile) | The AWS profile to use. | `string` | n/a | yes |
| <a name="input_rds_instance_class"></a> [rds\_instance\_class](#input\_rds\_instance\_class) | The RDS instance class to use. | `string` | `"db.m5.large"` | no |
| <a name="input_rds_postgres_allocated_storage"></a> [rds\_postgres\_allocated\_storage](#input\_rds\_postgres\_allocated\_storage) | The allocated storage for the RDS Postgres instance. | `number` | `20` | no |
| <a name="input_rds_postgres_db_name"></a> [rds\_postgres\_db\_name](#input\_rds\_postgres\_db\_name) | The name of the RDS Postgres database. | `string` | `"postgres"` | no |
| <a name="input_rds_postgres_iops"></a> [rds\_postgres\_iops](#input\_rds\_postgres\_iops) | The IOPS for the RDS Postgres instance. | `number` | `3000` | no |
| <a name="input_rds_postgres_name"></a> [rds\_postgres\_name](#input\_rds\_postgres\_name) | The name of the RDS Postgres instance. | `string` | `"postgres"` | no |
| <a name="input_rds_postgres_password"></a> [rds\_postgres\_password](#input\_rds\_postgres\_password) | The password for the RDS Postgres instance. | `string` | `"postgres"` | no |
| <a name="input_rds_postgres_snapshot_identifier"></a> [rds\_postgres\_snapshot\_identifier](#input\_rds\_postgres\_snapshot\_identifier) | The snapshot identifier for the RDS Postgres instance. | `string` | `""` | no |
| <a name="input_rds_postgres_storage_type"></a> [rds\_postgres\_storage\_type](#input\_rds\_postgres\_storage\_type) | The storage type for the RDS Postgres instance. | `string` | `"gp3"` | no |
| <a name="input_rds_postgres_username"></a> [rds\_postgres\_username](#input\_rds\_postgres\_username) | The username for the RDS Postgres instance. | `string` | `"postgres"` | no |
| <a name="input_region"></a> [region](#input\_region) | The AWS region to use. | `string` | `"us-gov-east-1"` | no |
| <a name="input_vpc_name"></a> [vpc\_name](#input\_vpc\_name) | The name of the VPC to create the RDS in. | `string` | n/a | yes |

## Outputs

No outputs.
<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
# flux-example
