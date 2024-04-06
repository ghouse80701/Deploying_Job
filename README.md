Ansible setup for aws:
======================
sudo  amazon-linux-extras install ansible2
ansible --version
sudo yum install python-pip
python --version
sudo pip install boto
sudo pip3 install boto3
sudo ansible-galaxy collection install amazon.aws


Things to be added in /etc/ansible/ansible.cfg
==============================================
[defaults]
inventory=/opt/aws_ec2.yaml     
host_key_checking=false
remote_user=ec2-user
private_key_file=/opt/key.pem

[inventory]
enable_plugins = aws_ec2

[privilege_escalation]
become=True
become_method=sudo
become_user=root

Aws Configuration
==============================================
aws configure
iam role of ec2fullaccess to be attached to ansible controller
