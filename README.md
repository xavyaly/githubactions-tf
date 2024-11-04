# githubactions-tf

# Create a github repo
'''
githubactions-tf
'''

# Configure aws
'''
aws configure
'''

# Terraform execution steps:
'''
terraform init

Initializing the backend...

Initializing provider plugins...
- Finding hashicorp/aws versions matching "~> 4.16"...
- Installing hashicorp/aws v4.67.0...
- Installed hashicorp/aws v4.67.0 (signed by HashiCorp)

Terraform has created a lock file .terraform.lock.hcl to record the provider
selections it made above. Include this file in your version control repository
so that Terraform can guarantee to make the same selections by default when
you run "terraform init" in the future.

Terraform has been successfully initialized!

You may now begin working with Terraform. Try running "terraform plan" to see
any changes that are required for your infrastructure. All Terraform commands
should now work.

If you ever set or change modules or backend configuration for Terraform,
rerun this command to reinitialize your working directory. If you forget, other
commands will detect it and remind you to do so if necessary.
$ terraform plan 

Terraform used the selected providers to generate the following execution plan. Resource actions are indicated
with the following symbols:
  + create

Terraform will perform the following actions:

  # aws_instance.web_server will be created
  + resource "aws_instance" "web_server" {
      + ami                                  = "ami-830c94e3"
      + arn                                  = (known after apply)
      + associate_public_ip_address          = (known after apply)
      + availability_zone                    = (known after apply)
      + cpu_core_count                       = (known after apply)
      + cpu_threads_per_core                 = (known after apply)
      + disable_api_stop                     = (known after apply)
      + disable_api_termination              = (known after apply)
      + ebs_optimized                        = (known after apply)
      + get_password_data                    = false
      + host_id                              = (known after apply)
      + host_resource_group_arn              = (known after apply)
      + iam_instance_profile                 = (known after apply)
      + id                                   = (known after apply)
      + instance_initiated_shutdown_behavior = (known after apply)
      + instance_state                       = (known after apply)
      + instance_type                        = "t2.micro"
      + ipv6_address_count                   = (known after apply)
      + ipv6_addresses                       = (known after apply)
      + key_name                             = (known after apply)
      + monitoring                           = (known after apply)
      + outpost_arn                          = (known after apply)
      + password_data                        = (known after apply)
      + placement_group                      = (known after apply)
      + placement_partition_number           = (known after apply)
      + primary_network_interface_id         = (known after apply)
      + private_dns                          = (known after apply)
      + private_ip                           = (known after apply)
      + public_dns                           = (known after apply)
      + public_ip                            = (known after apply)
      + secondary_private_ips                = (known after apply)
      + security_groups                      = (known after apply)
      + source_dest_check                    = true
      + subnet_id                            = (known after apply)
      + tags                                 = {
          + "Email" = "xyz@gmail.coom"
          + "Name"  = "Operations"
        }
      + tags_all                             = {
          + "Email" = "xyz@gmail.coom"
          + "Name"  = "Operations"
        }
      + tenancy                              = (known after apply)
      + user_data                            = (known after apply)
      + user_data_base64                     = (known after apply)
      + user_data_replace_on_change          = false
      + vpc_security_group_ids               = (known after apply)
    }

Plan: 1 to add, 0 to change, 0 to destroy.

────────────────────────────────────────────────────────────────────────────────────────────────────────────────

Note: You didn't use the -out option to save this plan, so Terraform can't guarantee to take exactly these
actions if you run "terraform apply" now.
$ 
$ terraform apply --auto-approve

Terraform used the selected providers to generate the following execution plan. Resource actions are indicated
with the following symbols:
  + create

Terraform will perform the following actions:

  # aws_instance.web_server will be created
  + resource "aws_instance" "web_server" {
      + ami                                  = "ami-830c94e3"
      + arn                                  = (known after apply)
      + associate_public_ip_address          = (known after apply)
      + availability_zone                    = (known after apply)
      + cpu_core_count                       = (known after apply)
      + cpu_threads_per_core                 = (known after apply)
      + disable_api_stop                     = (known after apply)
      + disable_api_termination              = (known after apply)
      + ebs_optimized                        = (known after apply)
      + get_password_data                    = false
      + host_id                              = (known after apply)
      + host_resource_group_arn              = (known after apply)
      + iam_instance_profile                 = (known after apply)
      + id                                   = (known after apply)
      + instance_initiated_shutdown_behavior = (known after apply)
      + instance_state                       = (known after apply)
      + instance_type                        = "t2.micro"
      + ipv6_address_count                   = (known after apply)
      + ipv6_addresses                       = (known after apply)
      + key_name                             = (known after apply)
      + monitoring                           = (known after apply)
      + outpost_arn                          = (known after apply)
      + password_data                        = (known after apply)
      + placement_group                      = (known after apply)
      + placement_partition_number           = (known after apply)
      + primary_network_interface_id         = (known after apply)
      + private_dns                          = (known after apply)
      + private_ip                           = (known after apply)
      + public_dns                           = (known after apply)
      + public_ip                            = (known after apply)
      + secondary_private_ips                = (known after apply)
      + security_groups                      = (known after apply)
      + source_dest_check                    = true
      + subnet_id                            = (known after apply)
      + tags                                 = {
          + "Email" = "xyz@gmail.coom"
          + "Name"  = "Operations"
        }
      + tags_all                             = {
          + "Email" = "xyz@gmail.coom"
          + "Name"  = "Operations"
        }
      + tenancy                              = (known after apply)
      + user_data                            = (known after apply)
      + user_data_base64                     = (known after apply)
      + user_data_replace_on_change          = false
      + vpc_security_group_ids               = (known after apply)
    }

Plan: 1 to add, 0 to change, 0 to destroy.
aws_instance.web_server: Creating...
aws_instance.web_server: Still creating... [10s elapsed]
aws_instance.web_server: Creation complete after 17s [id=i-070d9019efdfcd3a3]

Apply complete! Resources: 1 added, 0 changed, 0 destroyed.
$ terraform destroy --auto-approve
aws_instance.web_server: Refreshing state... [id=i-070d9019efdfcd3a3]

Terraform used the selected providers to generate the following execution plan. Resource actions are indicated
with the following symbols:
  - destroy

Terraform will perform the following actions:

  # aws_instance.web_server will be destroyed
  - resource "aws_instance" "web_server" {
      - ami                                  = "ami-830c94e3" -> null
      - arn                                  = "arn:aws:ec2:us-west-2:252473277340:instance/i-070d9019efdfcd3a3" -> null
      - associate_public_ip_address          = true -> null
      - availability_zone                    = "us-west-2b" -> null
      - cpu_core_count                       = 1 -> null
      - cpu_threads_per_core                 = 1 -> null
      - disable_api_stop                     = false -> null
      - disable_api_termination              = false -> null
      - ebs_optimized                        = false -> null
      - get_password_data                    = false -> null
      - hibernation                          = false -> null
      - id                                   = "i-070d9019efdfcd3a3" -> null
      - instance_initiated_shutdown_behavior = "stop" -> null
      - instance_state                       = "running" -> null
      - instance_type                        = "t2.micro" -> null
      - ipv6_address_count                   = 0 -> null
      - ipv6_addresses                       = [] -> null
      - monitoring                           = false -> null
      - placement_partition_number           = 0 -> null
      - primary_network_interface_id         = "eni-0631842c0a8c44eee" -> null
      - private_dns                          = "ip-172-31-24-2.us-west-2.compute.internal" -> null
      - private_ip                           = "172.31.24.2" -> null
      - public_dns                           = "ec2-34-211-177-142.us-west-2.compute.amazonaws.com" -> null
      - public_ip                            = "34.211.177.142" -> null
      - secondary_private_ips                = [] -> null
      - security_groups                      = [
          - "default",
        ] -> null
      - source_dest_check                    = true -> null
      - subnet_id                            = "subnet-070b34ee88c1fe521" -> null
      - tags                                 = {
          - "Email" = "xyz@gmail.coom"
          - "Name"  = "Operations"
        } -> null
      - tags_all                             = {
          - "Email" = "xyz@gmail.coom"
          - "Name"  = "Operations"
        } -> null
      - tenancy                              = "default" -> null
      - user_data_replace_on_change          = false -> null
      - vpc_security_group_ids               = [
          - "sg-017bab502ac04b90e",
        ] -> null

      - capacity_reservation_specification {
          - capacity_reservation_preference = "open" -> null
        }

      - cpu_options {
          - core_count       = 1 -> null
          - threads_per_core = 1 -> null
        }

      - credit_specification {
          - cpu_credits = "standard" -> null
        }

      - enclave_options {
          - enabled = false -> null
        }

      - maintenance_options {
          - auto_recovery = "default" -> null
        }

      - metadata_options {
          - http_endpoint               = "enabled" -> null
          - http_put_response_hop_limit = 1 -> null
          - http_tokens                 = "optional" -> null
          - instance_metadata_tags      = "disabled" -> null
        }

      - private_dns_name_options {
          - enable_resource_name_dns_a_record    = false -> null
          - enable_resource_name_dns_aaaa_record = false -> null
          - hostname_type                        = "ip-name" -> null
        }

      - root_block_device {
          - delete_on_termination = true -> null
          - device_name           = "/dev/sda1" -> null
          - encrypted             = false -> null
          - iops                  = 0 -> null
          - tags                  = {} -> null
          - throughput            = 0 -> null
          - volume_id             = "vol-0e490fd70bd45eb27" -> null
          - volume_size           = 8 -> null
          - volume_type           = "standard" -> null
        }
    }

Plan: 0 to add, 0 to change, 1 to destroy.
aws_instance.web_server: Destroying... [id=i-070d9019efdfcd3a3]
aws_instance.web_server: Still destroying... [id=i-070d9019efdfcd3a3, 10s elapsed]
aws_instance.web_server: Still destroying... [id=i-070d9019efdfcd3a3, 20s elapsed]
aws_instance.web_server: Still destroying... [id=i-070d9019efdfcd3a3, 30s elapsed]
aws_instance.web_server: Still destroying... [id=i-070d9019efdfcd3a3, 40s elapsed]
aws_instance.web_server: Still destroying... [id=i-070d9019efdfcd3a3, 50s elapsed]
aws_instance.web_server: Still destroying... [id=i-070d9019efdfcd3a3, 1m0s elapsed]
aws_instance.web_server: Still destroying... [id=i-070d9019efdfcd3a3, 1m10s elapsed]
aws_instance.web_server: Still destroying... [id=i-070d9019efdfcd3a3, 1m20s elapsed]
aws_instance.web_server: Still destroying... [id=i-070d9019efdfcd3a3, 1m30s elapsed]
aws_instance.web_server: Still destroying... [id=i-070d9019efdfcd3a3, 1m40s elapsed]
aws_instance.web_server: Still destroying... [id=i-070d9019efdfcd3a3, 1m50s elapsed]
aws_instance.web_server: Still destroying... [id=i-070d9019efdfcd3a3, 2m0s elapsed]
aws_instance.web_server: Still destroying... [id=i-070d9019efdfcd3a3, 2m10s elapsed]
aws_instance.web_server: Still destroying... [id=i-070d9019efdfcd3a3, 2m20s elapsed]
aws_instance.web_server: Still destroying... [id=i-070d9019efdfcd3a3, 2m30s elapsed]
aws_instance.web_server: Still destroying... [id=i-070d9019efdfcd3a3, 2m40s elapsed]
aws_instance.web_server: Still destroying... [id=i-070d9019efdfcd3a3, 2m50s elapsed]
aws_instance.web_server: Still destroying... [id=i-070d9019efdfcd3a3, 3m0s elapsed]
aws_instance.web_server: Still destroying... [id=i-070d9019efdfcd3a3, 3m10s elapsed]
aws_instance.web_server: Still destroying... [id=i-070d9019efdfcd3a3, 3m20s elapsed]
aws_instance.web_server: Still destroying... [id=i-070d9019efdfcd3a3, 3m30s elapsed]
aws_instance.web_server: Still destroying... [id=i-070d9019efdfcd3a3, 3m40s elapsed]
aws_instance.web_server: Still destroying... [id=i-070d9019efdfcd3a3, 3m50s elapsed]
aws_instance.web_server: Still destroying... [id=i-070d9019efdfcd3a3, 4m0s elapsed]
aws_instance.web_server: Still destroying... [id=i-070d9019efdfcd3a3, 4m10s elapsed]
aws_instance.web_server: Still destroying... [id=i-070d9019efdfcd3a3, 4m20s elapsed]
aws_instance.web_server: Still destroying... [id=i-070d9019efdfcd3a3, 4m30s elapsed]
aws_instance.web_server: Still destroying... [id=i-070d9019efdfcd3a3, 4m40s elapsed]
aws_instance.web_server: Destruction complete after 4m43s

Destroy complete! Resources: 1 destroyed.
'''

# Configuration Steps:
'''
Click on "Actions" 
Click on "Terraform" 
Click on "configure" -> terraform.yml
Click on "Commit changes..."
'''

# New file created:
'''
.github/workflows/terraform.yml
'''

# Pull the changes to local
'''
git pull 
remote: Enumerating objects: 6, done.
remote: Counting objects: 100% (6/6), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 5 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (5/5), 2.37 KiB | 347.00 KiB/s, done.
From https://github.com/xavyaly/githubactions-tf
   8e0c31d..97d6540  main       -> origin/main
Updating 8e0c31d..97d6540
Fast-forward
 .github/workflows/terraform.yml | 93 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
 1 file changed, 93 insertions(+)
 create mode 100644 .github/workflows/terraform.yml
'''

# Remove the unwanted content and push to remote
'''
In case if interested
'''

# Add a new line and push the changes on main branch, new commit id created and job executed
'''
https://github.com/xavyaly/githubactions-tf/actions/runs/11662087827/job/32467728371
'''





