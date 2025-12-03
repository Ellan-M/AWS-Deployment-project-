# DevOps Lab: Server Automation

## Infrastructure
- 3 Ubuntu EC2 instances
- SSH key-based authentication
- Security group: SSH (22), HTTP (80)

## Installed Components
- Nginx: Web server
- Git: Version control
- UFW: Firewall
- Fail2ban: Intrusion prevention

## Files
- `setup-server.sh`: Bash installation script
- `ansible-playbook/playbook.yml`: Ansible automation
- `ansible-playbook/inventory.ini`: Server inventory

## Usage
```bash
# Run bash script
./setup-server.sh

# Run ansible playbook
ansible-playbook -i inventory.ini playbook.yml
```

## Verification Commands
```bash
# Check all services
ansible webservers -i inventory.ini -m shell -a "systemctl is-active nginx fail2ban" -b

# Check firewall
ansible webservers -i inventory.ini -m shell -a "ufw status" -b
```