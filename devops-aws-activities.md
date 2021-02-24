# DevOps AWS Activities

GitHub Activities:
* Fork repo from github

EC2 Activities:
* Create EC2 instance based on SecureAmazonLinux2
* Install nginx, clone repo from your GitHub, update app html
* Test: Troubleshoot access in sec group
* Note: you could als write a bash script and use user_data for bootstrapping

Architecture Diagram:
* EC2 inside VPC with sec group

S3 Activites:
* Create bucket and upload a test.txt file
* Problem: How to upload images from EC2 to S3 bucket? credentials or role?
* Best practice for communication between services in AWS?

IAM Activities:
* How to create IAM S3 Role?

EC2 Activities:
* Attach IAM S3 Role to your EC2 instance
* Test: Check if you can list your bucket contets

S3 Activities:
* Upload images to S3 Bucket using CLI

GitHub Activities:
* Update images from app

EC2 Activities:
* Update your app hmtl
* Problem: Why images doesn't work?

S3 Activities:
* Enable public read
* Note: You can secure the images to be accesible only from your site instead of S3 public

Architecture Diagram:
* EC2 inside VPC with sec group
* IAM Role for EC2 for S3 access

ELB Activities:
* Create ELB, and attach EC2 Instance
* Enable access through ELB
* Problem: What happens if we need to add another instance? do we need to configure it again?

EC2 Activities:
* Create AMI with preconfigured stuff
* Create and launch an additional instance
* Problem: What happens your instance is down?

ELB Activities:
* Attach your new EC2 instance to ELB
* Test: Stop one instance and check if your site is still available
* Problem: What happens if we want to grow dinamically or recover from failure?

Architecture Diagram:
* EC2 inside VPC with sec group
* IAM Role for EC2 for S3 access
* ELB with 2 instances

AutoScaling:
* Delete ELB and EC2 instances (Don't worry you have an AMI, cattle not pets)
* Create AutoScaling Configuration
* Create AutoScaling Group with your AMI
* Test: Stop one instance and check if your site is still available, verify that a new instance has been launched
* Note: You can automate all this process with Cloudformation or Terraform

Architecture Diagram:
* EC2 inside VPC with sec group
* IAM Role for EC2 for S3 access
* AutoScaling Group
* ELB with 2 instances
