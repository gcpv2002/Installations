# Installing Tomcat on Linux
## To install Tomcat(9 or 10) on Linux, follow the steps below:
### Replace "(Version)" with the tomcat version required

To update the system, use the command
```
sudo apt update && sudo apt upgrade -y
```

----------
**Only if installing Tomcat9 👇**

If insatalling Tomcat9, add the repository that contains Tomcat 9. To do that, use the command
```
sudo add-apt-repository "deb http://archive.ubuntu.com/ubuntu/ jammy main universe"
```
To update the package index, use the command
```
sudo apt update
```
----------


To install Tomcat(Version) along with documentation and admin tools, use
```
sudo apt install -y tomcat(Version) tomcat(Version)-docs tomcat(Version)-admin
```

Copy the admin applications to the Tomcat webapps directory. To do that, use the command
```
sudo cp -r /usr/share/tomcat(Version)-admin/* /var/lib/tomcat(Version)/webapps/ -v
```

To edit the Tomcat users configuration file, use the command
```
sudo vi /var/lib/tomcat(Version)/conf/tomcat-users.xml
```
Scroll to the bottom and add the following lines before ```</tomcat-users>```:
```
<role rolename="manager-gui"/>
<role rolename="admin-gui"/>
<role rolename="manager-script"/>
<user username="tomcat" password="tomcat" roles="admin-gui,manager-gui,manager-script"/>
```
Save and exit the file.

To apply the changes, restart Tomcat using
```
sudo systemctl restart tomcat(Version)
```

To verify Tomcat status, use the command
```
sudo systemctl status tomcat9
```