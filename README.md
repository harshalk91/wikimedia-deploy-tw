# wikimedia-deploy
Demo deployment for wikimedia

Steps:
1. Install python3, Ansible: 2.10.2, Terraform: 0.14.4, 
2. pip3 install sshpass jmespath
3. Edit deployment/terraform/main.tf and enter following
   1. aws_access_key
   2. aws_secret_key
   3. aws_region
   4. ami (centos 7 preferable)
   5. instance)type
   6. vpc_security_group_ids
   7. subnet_id
   8. key_name
4. traverse to deployment/terraform
5. terraform init
6. terraform plan
7. terraform apply
8. Traverse to deployment
9. Export aws access, secret and region
10. Edit ec2.ini file (regions, instance_filters = tag:type="wikimedia-demo")
11. ansible-playbook -i ec2.py site.yml
12. Access wikimedia using http://ip:port
