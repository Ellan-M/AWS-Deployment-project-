This project demonstrates the deployment of a Web Application on AWS Using EC2, Ansible Automation, Classic Load Balancer, and S3


This project was part of my learning journey in cloud engineering, where I tested and strengthened my automation, troubleshooting, and infrastructure design skills.


Project Architecture

The deployment covers:

- Two EC2 Ubuntu servers configured using Ansible
- NGINX installed and configured automatically
- A Classic Load Balancer routing traffic across both servers
- S3 Static Hosting used to compare hosting performance and cost
- Security Groups, SSH keys, health checks, and automation scripts

---

Technologies Used

- AWS EC2
- AWS S3
- AWS Classic Load Balancer
- Ubuntu 22.04 LTS
- Ansible
- NGINX
- HTML 

---


```bash
sudo apt update
sudo apt install ansible -y
ansible --version

- Deploying two EC2 instances running Ubuntu
- Configuring servers using Ansible
- Deploying NGINX via Playbook
- Setting up a Classic Load Balancer
- Hosting a static website on S3

## How To Run

1. Update `host-inventory` with your IPs
2. Run `ansible-playbook -i host-inventory playbook.yml`
3. Test your EC2 public IPs
4. Open the Load Balancer DNS
5. Test S3 static hosting

For a more detailed breakdown, check my medium post [https://medium.com/@mercyodoh25/deploying-a-web-application-on-aws-using-ec2-with-automation-ansible-load-balancer-and-s3-b6563f3fb7ff]