# Jenkins Installation

# Installing Jenkins on Linux

## Prerequisites
- Ubuntu 20.04 LTS (or any other compatible Linux distribution)
- sudo access to run commands with root privileges

## Steps

### 1. Update Package Index
Before installing Jenkins, it's good practice to ensure that your system's package index is up-to-date.
```
sudo apt update
```
2. Install Java
Jenkins requires Java to be installed on your system. OpenJDK is recommended.
```
sudo apt install openjdk-11-jdk
```
3. Add Jenkins Repository Key
Add the repository key to your system to trust packages from the Jenkins repository.

bash
Copy code
wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -
4. Add Jenkins Repository
Add the Jenkins repository to your system's list of package sources.

bash
Copy code
sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
5. Update Package Index Again
After adding the Jenkins repository, update the package index again to include Jenkins packages.

bash
Copy code
sudo apt update
6. Install Jenkins
Finally, install Jenkins using the following command.

bash
Copy code
sudo apt install jenkins
7. Start Jenkins Service
Once installed, start the Jenkins service.

bash
Copy code
sudo systemctl start jenkins
8. Enable Jenkins Service (Optional)
If you want Jenkins to start automatically at boot, enable the service.

bash
Copy code
sudo systemctl enable jenkins
9. Grant Root Access to Jenkins User
To allow the Jenkins user to execute commands with root privileges (optional, but useful for certain configurations), use the usermod command.

bash
Copy code
sudo usermod -aG sudo jenkins
10. Access Jenkins
You can now access Jenkins in your web browser by navigating to http://your_server_ip_or_domain:8080.

11. Unlock Jenkins
Upon first access, you'll be prompted to unlock Jenkins. Follow the instructions displayed on the screen.

12. Install Recommended Plugins (Optional)
You can either install recommended plugins or select plugins to install manually based on your requirements.

13. Create Admin User
After installing plugins, create an admin user for Jenkins.

14. Start Using Jenkins
Once configured, you can start using Jenkins for your CI/CD needs.
