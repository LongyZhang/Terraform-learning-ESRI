1   Type of Infrastructure as code tools?

    1: Configuration management "Ansible, puppet, saltstack"
    2: Server templating "Docker, Packer, Vagrant"
    3: Provisioning tools "Terraform, CloudFormation"

1   What is Terraform?

    1: free and open source tool which is developed by hashcrop
    2: it can deploye the IAC across muti platform such as physicial machines, VMware, AWS, GCP and Azure
    3: Teeraform uses the HashiCorp Configuration language

1   What is Desire Sate and current state?  

    1: Terraform can deploye the Resired state into current state, Desired state stands for current .tf file, the current state stands for current infrastructure Configuration 

1   The structure of HCL file (.tf extension file)

    1: <block> <"parameters tpye, paramters name"> {
        key1 =  value1
        key2 =  value2
        (argument) = (value)
    }
    2: resource "local_files" "pet" {
        filename="/root/pets.txt"
        content = "we love pets"
    }
    3: resource "aws_instance" "webserver"{
        ami= "ami-xxxxx"
        instance_type = "t2.micro"
    }

    4: resource "aws_s3_bucket" "date" {
        bucket = "webserver-bucket-xxx"
        acl ="private"
    }

1   the workflow of terraform

    1: Write terraform file (.tf extension)
    2: terraform init (terraform file initilization)
    3: terraform plan (review execution plan)
    4: terraform apply (apply terraform changes to platform )
    5: terraform show (it shows the terraform config under current folder)

1   What is basic usage of terraform?
    
    1: terraform init (initialize the backend)
    2: terraform plan ()
    3: terraform apply
    4: terraform destory
 

2   what is prerequesite of terraform? and how to establish connection between aws and terraform? 

    1: create your own acocunt in AWS
    2: create user group and add policy
    3: create user
    4: create main.tf sample, 
    5: install aws command line (aws cli)
    6: run "aws configure", pass your access id and secret key

3   what is terraform state file?

    1: it stands for Terraform's representation of world
    2: it is Json file format, it contains every resource and data object
    3: it contains sensitive info (e.g. database password)
    4: it can be store remotely and locally

4   How does terraform plan, apply and destroy work? 

    1: it is meant to do comparsion between terraform config(Desire state) and terraform state(acatual state)
    if found the difference == true
        notify the AWS provider
        then
        using the terraform apply to add service to AWS provider (e.g. add virtual machine)   

    Terraform destroy -> it can destroy the all of resource as associate with this project
    
5   What is S3 Bucket? 
    1: Amazon Simple Storage Service is object storing service 
    ![image](https://user-images.githubusercontent.com/101307724/207036366-4d8a0b00-5ef3-4ec5-8fb2-2f4cfcbaebd6.png)

6   Type of Infrastructure as code tools?

    1: Configuration management "Ansible, puppet, saltstack"
    2: Server templating "Docker, Packer, Vagrant"
    3: Provisioning tools "Terraform, CloudFormation"


