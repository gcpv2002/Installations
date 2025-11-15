# Installing Docker on Linux
## To install Docker on Linux, follow the steps below:

To update the system, use the command
```
sudo apt update && sudo apt upgrade -y
```

To install Docker, use the command
```
sudo apt install docker.io
```

To run Docker without sudo, use the command
```
sudo usermod -aG docker $USER
```
replace "$USER" with the username of your machine

To check the version, use the command
```
docker --version
```

To start Docker, use the command
```
systemctl start docker
```

To enable Docker, use the command
```
sudo systemctl enable docker
```

To verify the status of Docker, use the command
```
systemctl status docker
```