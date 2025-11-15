# Installing Trivy on Linux
## To install Trivy on Linux, follow the steps below:

To update the system, use the command
```
sudo apt update && sudo apt upgrade -y
```

Trivy requires wget, apt-transport-https, gnupg, and lsb-release. To install them, use the command
```
sudo apt-get install wget apt-transport-https gnupg lsb-release
```

To trust the Trivy repository, add its GPG key, use the command
```
wget -qO - https://aquasecurity.github.io/trivy-repo/deb/public.key | sudo apt-key add -
```

To add the Trivy repository to your system, use the command
```
echo deb https://aquasecurity.github.io/trivy-repo/deb $(lsb_release -sc) main | sudo tee -a /etc/apt/sources.list.d/trivy.list
```

After adding the repository, update the package list
```
sudo apt-get update
```

Install Trivy using the following command
```
sudo apt-get install trivy -y
```

To check the status of Trivy, use the command
```
trivy --version
```