# UiRobot-GCP-Terraform
 UiPath Robot GCP deployment via Terraform.

 [![button](http://gstatic.com/cloudssh/images/open-btn.png)](https://console.cloud.google.com/cloudshell/open?git_repo=https://github.com/hteo1337/UiRobot-GCP-Terraform&tutorial=README.md)

## Installing Terraform
Please check : https://learn.hashicorp.com/terraform/getting-started/install.html


 
## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-----:|:-----:|
| region | Region | string | `"us-west1"` | yes |
| az | Availability Zone | string | `"us-west1-a"` | yes |
| image | GCP instances image | string | `"windows-server-2016-dc-v20190620"` | yes |
| vm\_type | Machine type : CPU and RAM size. See https://cloud.google.com/compute/docs/machine-types | string | `"n1-standard-4"` | yes |
| instance\_count | Number of robots to be created. | string | `"2"` | yes |
| disk\_size | Disk size for each VM. | string | `"50"` | yes |
| app\_name | Base VM name. | string | `"uirobot"` | yes |
| set\_local\_adminpass | Set local admin password. | string | `"yes"` | yes |
| admin\_password | Local windows administrator password. If variable 'set_local_adminpass' is 'yes'. | string | `"Local@dminP@55!*"` | yes |
| robot\_local\_account\_role | Robot local accout role : localadmin or localuser | string | `"localadmin"` | yes |
| orchestrator\_url | orchestrator url | string | `"https://corp-orchestrator.com"` | yes |
| orchestrator\_tennant | orchestrator tennant | string | `"default"` | yes |
| orchestrator\_admin | orchestrator admin username | string | `"admin"` | yes |
| orchestrator\_adminpw | orchestrator admin password | string | `"Orc@dminP@55!*"` | yes |
| vm\_username | Robot VM username | string | `"uirobot"` | yes |
| vm\_password | Robot VM password | string | `"UiRobot@dminP@55!"` | yes |
| robot\_type | Robot type | string | `"Unattended"` | yes |

## Outputs

| Name | Description |
|------|-------------|
| public\_ip | Output variable: Public IP address |

