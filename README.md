## Running The Application In Our Machine  :

STEPS :
1. Clone the repo
 ``` bash
   git clone
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

## Running The Application In EC2 :

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
           Downloads external libraries (packages)
           Stores them in node_modules/
           Makes them available to Node.js
 ```bash
 sudo apt update
 sudo apt install -y nodejs npm git
 node -v
 npm -v
 git --version
```
5. clone the repo :
 ``` bash
  git clone
  cd  Running-Small-Application-in-EC2
```
6. Run the application
``` bash
npm install
npm run start
```
ACCESS THE APPLICATION AT :
 http://<ec2-ip>:3000
 




