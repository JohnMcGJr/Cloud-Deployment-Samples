# Qumulo Cloud Deployment Samples
Samples for deploying Qumulo Core in AWS using popular orchestration
technologies.  Right now we have a sample template for Terraform, and a script to generate a custom AWS CloudFormation template but please open an issue or PR and we'll add your favorite orchestration technology.

## Terraform
www.terraform.io

`qumulo.tf` contains a terraform template for deploying Qumulo clusters.  Set
the number of nodes in the `cluster_config` variable (4+ nodes only).
A tfvars file can be used to provide the necessary variables from your
environment.

## CloudFormation
https://aws.amazon.com/cloudformation/

`generate_qcft.py` contains a python script that generates an AWS CloudFormation
template (CFT) with the desired number of nodes and instance names. The CFT that 
is generated will contain a preconfigured AWS Security Group that enables the 
cluster to serve clients as well as opens ports for management, replication, 
and clustering.

An example of the ouput of this script is provided in the file `qcft.json`.