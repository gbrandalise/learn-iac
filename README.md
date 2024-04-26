# Install Terraform:
```sh
  wget -O- https://apt.releases.hashicorp.com/gpg | gpg --dearmor | sudo tee /usr/share/keyrings/hashicorp-archive-keyring.gpg
  echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
  sudo apt update && sudo apt install terraform
```

# Install Python:
```sh
  sudo apt install python3
```
  
# Install Ansible:
```sh
  sudo apt update
  sudo apt install software-properties-common
  sudo add-apt-repository --yes --update ppa:ansible/ansible
  sudo apt-get install ansible
```
  
# Install aws cli:
```sh
  curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
  unzip awscliv2.zip
  sudo ./aws/install
```
  
# Configure aws cli:
```sh
  aws configure
```sh
  1. access key id: id do access key
  2. access secret key: access key gerado
  3. region: sa-east-1
  
# Terraform/Ansilbe commands:
```sh
  cd aws
  terraform init
  terraform plan
  terraform apply
  chmod 400 iac-alura.pem
  ssh -i "iac-alura.pem" ubuntu@ec2-18-228-116-189.sa-east-1.compute.amazonaws.com
  ansible-playbook -i hosts -u ubuntu --private-key /mnt/c/Users/giovannybrandalise/.ssh/iac-alura.pem playbook.yml
  terraform destroy
```
