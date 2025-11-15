# Installing Terraform on Linux
## To install Terraform on Linux, follow the steps below:

To update the system, use the command
```
sudo apt update && sudo apt upgrade -y
```

Terraform requires wget and unzip. If not already done, use the command
```
sudo apt install -y wget unzip
```

To download Terraform, use the command
```
wget https://releases.hashicorp.com/terraform/1.7.0/terraform_1.7.0_linux_amd64.zip
```
If a specific release is required, navigate to [Terraform official release page](https://releases.hashicorp.com/terraform) and modify the link in the above command

To unzip the downloaded file, use the command
```
unzip terraform_1.7.0_linux_amd64.zip
```

To move Terraform to a directory in your PATH, use the command
```
sudo mv terraform /usr/local/bin/
```

To check the version, use the command
```
terraform -v
```