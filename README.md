# Installations
Create EC2 instane 
Connrect to EC2 from local window (mobaxterm)
>  chmod 600 pem file location(/drives/c/Users/hchar/Downloads/AWS) pemfile name
>  ssh -i  pemfilelocation(/drives/c/Users/hchar/Downloads/AWS/EC2_keyvaluepair.pem) ubuntu@54.89.232.114(EC2 public IP)
>  Install AWS cli :  sudo snap install aws-cli --classic


# Steps to install Jenkins..

Prequisit: install java on instance before installinh Jenkins
sudo apt update
sudo apt install fontconfig openjdk-17-jre
java -version
openjdk version "17.0.13" 2024-10-15
OpenJDK Runtime Environment (build 17.0.13+11-Debian-2)
OpenJDK 64-Bit Server VM (build 17.0.13+11-Debian-2, mixed mode, sharing)

# Or if in root user use below command directly from below
wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]" \
  https://pkg.jenkins.io/debian-stable binary/ |  tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
 apt-get update
 apt-get install jenkins

# check Jenkin Status
 systemctl status jenkins

 Jenkins run on 8080 port and can be accessed over http://54.89.232.114:8080/ (http://ec2 publicIP:8080)

# Modify security rule for access 
Inbound rules
EC2
Security Groups
sg-015352e25bbc4a29d - launch-wizard-1 Edit inbound rules

 
