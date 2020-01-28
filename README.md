# Rekognition
Making a face recognition system by using AWS Rekognition API

## In this project we are going to deploy 3 servers on AWS Cloud:
- Frontend on Apache web server
- Backend using flask package
- Database storage

Let's start with Frontend
## Frontend
- EC2 instance: Ubuntu free tier
- Attach to VPC and Public Subnet
- Security Group: TCP 22 from your IP, HTTP 80, Custom TCP 5000
- Connect to EC2 instance
``ssh -i "<your_keypair.pem>" ubuntu@<PublicIPaddress_of_EC2``
- Installation of Apache server:
 ```
 apt-get update
 sudo apt install apache2
 sudo ufw allow 'Apache'
 sudo ufw status
 sudo systemctl status apache2
 ```
- Go to your EC2 instance using Public IP on browser
- You should see picture as below if it is properly installed:
![Apache](Apache.png)
- Copy files from repository including index.html and Static folder to EC2 instance's folder /var/www/html/. In my case, I used WinSCP to copy  files
![WinSCP](WinSCP.png)
- Allow browser to execute your webcam visiting link: *chrome://flags/#unsafely-treat-insecure-origin-as-secure*, paste your Public IP and click on button *enabled*


Permission:
sudo chown -R ubuntu:ubuntu .



Backend
you might want to try this:

for anaconda 2 :
``export PATH=~/anaconda2/bin:$PATH``

for anaconda 3 :
``export PATH=~/anaconda3/bin:$PATH``

# Suggest as attendance check at University
