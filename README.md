# Ansible Workshop - Ansible Workshop using VSCode

Some customers are unable to access Ansible Workshops via SSH. Coder.com has open sourced its cloud-server component which allows VSCode to run on a remote server fully accessible through the browser. 

# Setup
First provision the correct number of environments using RHPDS and wait until the provisioning process is complete. Once complete, login to the first student server using the ip address and password found in http://{GUID}.rhdemo.io. 

> Note, you will need to perform this for each lab environment.

> Note, verify you are pulling down the latest version of code-server https://github.com/codercom/code-server/releases/latest
Enter the correct version for each of the below lines, examples are for 2.1692-vsc1.39.2: 
```
wget https://github.com/codercom/code-server/releases/download/{version}/code-server-{version}-linux-x64.tar.gz
```
```
tar -xvzf code-server-{version}-linux-x64.tar.gz
```
```
cd code-server-{version}-linux-x64
```
Using 2.1692-vsc1.39.2 as an example
```
wget https://github.com/cdr/code-server/releases/download/2.1692-vsc1.39.2/code-server2.1692-vsc1.39.2-linux-x86_64.tar.gz
```
Then untar the file
```
tar -xvzf code-server2.1692-vsc1.39.2-linux-x86_64.tar.gz 
```
Next move to that directory
```
cd code-server2.1692-vsc1.39.2-linux-x86_64
```
Make sure you have the appropriate permisions
```
chmod +x code-server
```
Run the code-server without a password so students can log directly in
```
nohup ./code-server --auth none &
```
They can then login to the terminal using the IP address and port 8080
```
http://{ipaddr}:8080/
```
You can add an Ansible extension to VS Code to provide syntax highlighting and autocomplete. Select Extensions, then in the extensions search bar in the top left, type Ansible. Find the extension titled "Ansible" 0.5.2 VS Code extension for Ansible. And click Install.

For students: once the window opens, click the 3 horizontal bars in the top left, hover over terminal and select "New Terminal"

Now begin the lab starting with the portion after logging in to the control host.

---

![Ansible logo](https://github.com/ansible/workshops/raw/master/images/rh-ansible-automation.png)
