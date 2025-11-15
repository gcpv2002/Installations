# Installing Jenkins on Linux
## To install Jenkins on Linux, follow the steps below:

To update the system, use the command
```
sudo apt update && sudo apt upgrade -y
```

Jenkins requires Java 17 to run. To install Java, use the command
```
sudo apt install -y openjdk-17-jdk
```

To check java version, use the command
```
java -version
```

To download Jenkins packages, first add the Jenkins key
```
sudo wget -O /etc/apt/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
```
Add the Jenkins repository to your system
```
echo "deb [signed-by=/etc/apt/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian-stable binary/" \
  | sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null
```

Update the package index after adding the repository using the command
```
sudo apt update
```

To install Jenkins, use the command
```
sudo apt install -y jenkins
```

To start Jenkins and enable it to run on boot, use the commands
```
sudo systemctl start jenkins
sudo systemctl enable jenkins
```

To check the version, use the command
```
jenkins --version
```

To check the status of Jenkins, use the command
```
sudo systemctl status jenkins
```