# Auto Provision of Jenkins on AWS

Terraform code to automate the provisioning of Jenkins master on AWS EC2 instance.

* Before executing terraform apply command, login aws console and create a KeyPair and downlaod the 
publickey (*.pem). This key is associated with ec2 instance and will be used to ssh to 
ec2 instance whenever it is needed.

* Once the key is generated then add as keyname. Please ensure the keypair must be created in the same region that you are 
going to provide ec2 instance.

* Please modify the backend.tf to store the state file remotely in S3 buckets.

Note: Finally dont forget to run "terraform destroy auto-approve" command to remove the resources you created 
via terraform, otherwise you will be charged by AWS for running resources.