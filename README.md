# EFS(Elastic File Sysytem)

* Launched an EC2 instance on aws, used http sever to lauch a simple website.
* Stored the static part of website code in s3 bucket and used cloudfront to access it.
* Used Efs for storage so that even after the Ec2 instance crashes the code of website intact .
* We can launch another instance and attach The Efs storage  to get our data back.

## Installation

*  <a href="https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html">Download aws cli</a>

* <a href="https://www.terraform.io/downloads.html">Download Terraform</a>

* To login to aws from Cli
```bash
aws configure
```
It will ask the secret key, access key and the region.The access and secret key can be obtained from Aws dashboard.

* Install terraform and make a profile in aws so as to not expose our secret key
```
aws configure --profile sahil
```
It will ask for secret key and access key.

* Initialize a folder with 

```
terraform init
```
* Run the below command to run the code

```
terraform apply --auto-approve
```