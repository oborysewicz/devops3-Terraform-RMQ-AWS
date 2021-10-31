# devops3-Terraform-RMQ-AWS
## My First DevOps Button Click Environment Build

We really want to automate as many services as we can so that when catastrophe hits, we can quickly destroy and rebuilt with as few clicks as possible and in theory minimal experience required.  If the least technical person in the room can't rebuild your service, then you haven't automated enough.

## Environment & Technologies used in this project
* GCP (Cloud Provider 1): Ubuntu instance as my work desktop machine and Ansible & Jenkins server all in one
* This GitHub repository as my terraform and ansible files container 
* Terraform for my Infrastructure as Code
* Ansible for my server configuration (With Dynamic Inventory for our RMQ EC2)
* Jenkins host and jobs to Deploy the Terraform and ansible files. Jenkins pulls my Terraform files from Github on deploy and Plan, Apply or Destroy my RabbitMQ instance. Jenkins also pulls my Ansible reqs from GitHub as well on deploy and run the playbooks from RMQ Setup when needed.
* AWS (Cloud Provider 2): RabbitMQ instance in EC2 automatically deployed by Terraform and configured by Ansible using Jenkins jobs
