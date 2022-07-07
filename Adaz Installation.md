# Adaz

[Adaz github page](https://github.com/christophetd/Adaz)

# Installation
- Install Prerequisites (Azure CLI and terraform)
```
cd ~
curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash

curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo apt-key add -
sudo apt-add-repository "deb [arch=amd64] https://apt.releases.hashicorp.com $(lsb_release -cs) main"
sudo apt-get update && sudo apt-get install terraform
az login
```
-   Clone this repository
```
git clone https://github.com/christophetd/Adaz.git
```
# Running Adaz
-   Navigate to Adaz and create a virtual env to install Ansible dependencies
```
cd Adaz
python3 -m venv ansible/venv 
source ansible/venv/bin/activate
pip install -r ansible/requirements.txt
export PATH=$PATH:$(pwd)/ansible/venv/bin
```

-   Change your credentials in domain.yml (Optional but recommended
    
-   Initialize Terraform
```
cd terraform
terraform init && terraform apply
```
