# AWS-Driver-Config

This project was developed to test the configuration of ODBC drivers
to connect to different data sources, such as AWS Athena through ODBC and
the Denodo Virtual Data Platform.

The build of the Amazon Machine Image is done through Packer and the 
deployment of the EC2 instance is covered by Terraform.

---

Below we have an example of the `terraform.tfvars` file that may need to
be created at the root of the directory. The stack is in itself pretty much
automated, but some knowledge of Terraform will come in handy.

```terraform
region = "us-east-1"
instance_type = "t3.medium"
ebs_size = "20"
ec2_ami = "ami-020293c91322b236d"
ingress_cidr_blocks = "0.0.0.0/0"
```