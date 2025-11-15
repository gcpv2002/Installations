# Installing kubectl (Kubernetes-CLI) on Linux
## To install kubectl (Kubernetes-CLI) on Linux, follow the steps below:

To update the system, use the command
```
sudo apt update && sudo apt upgrade -y
```

To download the latest release of kubectl, use the command
```
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
```

To make it executable, use the command
```
chmod +x kubectl
```

To move it into your PATH, use the command
```
sudo mv kubectl /usr/local/bin/
```

To check the version, use the command
```
kubectl version --client
```