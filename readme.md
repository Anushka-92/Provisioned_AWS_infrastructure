
# Provisioned AWS Infrastructure Can be created using following steps:
1.Created VPC & Subnet

2.Created custom Route Table
 
 3.Added Subnet Association with Route Table
 
 4.Configured Default/Main Route Table

 5.Created Security Group
 
 6.Configured Default Security Group
 
 7.Created EC2 Instance
- Fetch AMI
  
- Create ssh key-pair and download .pem file
  
- restrict permission
  
 8.SSH into EC2 instance
 
 9.Automated ssh key-pair - configured ssh key pair in Terraform config file
 
 10.Configured Terraform to install Docker and run nginx image, extracted shell commands to own shell script
 
 11.Accessed nginx through Browser


--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Important Terraform Commands:
### initialize

    terraform init

### preview terraform actions

    terraform plan

### apply configuration with variables

    terraform apply -var-file terraform-dev.tfvars

### destroy a single resource

    terraform destroy -target aws_vpc.myapp-vpc

### destroy everything fromtf files

    terraform destroy

### show resources and components from current state

    terraform state list

### show current state of a specific resource/data

    terraform state show aws_vpc.myapp-vpc    

### set avail_zone as custom tf environment variable - before apply

    export TF_VAR_avail_zone="eu-west-3a"

### set aws configuration through env variables

    export AWS_ACCESS_KEY_ID="anaccesskey"
    export AWS_SECRET_ACCESS_KEY="asecretkey"
    export AWS_DEFAULT_REGION="us-west-2"

