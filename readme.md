### Provisioned AWS Infrastructure Can be created using following steps:
Created VPC & Subnet
❏ Created custom Route Table
❏ Added Subnet Association with Route Table
❏ Configured Default/Main Route Table
❏ Created Security Group
❏ Configured Default Security Group
❏ Created EC2 Instance (Fetch AMI, Create ssh key-pair and download .pem 
file and restrict permission)
❏ SSH into EC2 instance
❏ Configured ssh key pair in Terraform config file
❏ Created EC2 Instance
- Fetch AMI
- Create ssh key-pair and download .pem file
- restrict permission 
❏ SSH into EC2 instance
❏ Automated ssh key-pair - configured ssh key pair in Terraform config file
❏ Configured Terraform to install Docker and run nginx image
❏ Extract shell commands to own shell script
❏ Accessed nginx through Browser





### Important Terraform Commands:
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

