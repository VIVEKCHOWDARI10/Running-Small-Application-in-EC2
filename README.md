## Run The Application In Our Machine  :

STEPS :
1. Clone the repo
 ``` bash
   git clone https://github.com/VIVEKCHOWDARI10/Running-Small-Application-in-EC2.git
   ```
2. Install the  Dependencies
``` bash
cd Running-Small-Application-in-EC2/
npm install
```
3. Run The Application :
 ``` bash
 npm run start
```
ACCESS AT :
http://localhost:3000

## Run The Application In EC2 :

STEPS :

1. Create an EC2 Instance in the AWS and  download the  key pair which is used to ssh the ec2 instance
2. Now ssh the ec2 :

   Move to the .pem downloaded file directory 
``` bash
 cd Downloads
```
``` bash
 chmod 400 <keypair-name>.pem
``` 
``` bash
 ssh -i keypair-name.pem ubuntu@<ip-of-ec2>
```
3. Now you are in the ec2 instance
4. Download the nodejs, npm, git
   
   Your application code is written in JavaScript.
  
    👉 Node.js is the software that understands and runs JavaScript code on the server.( interprets / executes )
   
    👉 npm is used to install and manage the external packages required by the application.
   
      npm = Node Package Manager
        It:
           Downloads external libraries (packages),
           Stores them in node_modules
   
   
 ```bash
 sudo apt update
 sudo apt install -y nodejs npm git
 node -v
 npm -v
 git --version
```
5. clone the repo :
 ``` bash
  git clone  https://github.com/VIVEKCHOWDARI10/Running-Small-Application-in-EC2.git
  cd  Running-Small-Application-in-EC2
```
6. Run the application
``` bash
npm install
npm run start
```
ACCESS THE APPLICATION AT :
 http://localhost:3000      #here localhost will be the ec2 instance ip 


## WHY ERROR (IMPORTANT)?
![App Running](<img width="1470" height="823" alt="screenshot" src="https://github.com/user-attachments/assets/e05c242c-c434-475d-8416-fc957e42b617" />
.png)

 7. We didnt add the INBOUND RULES in our instance 
 
   Go to the security groups and add new INBOUND RULE  with port 3000 and source 0.0.0.0/0 
   
 




