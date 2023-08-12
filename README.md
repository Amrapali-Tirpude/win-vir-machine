# win-vir-machine
# windows virtual machine
#aws mini project
#Deploy a Windows virtual machine on AWS
STEPS TO DEPLOY A WINDOWS VIRTUAL MACHINE BY USING AWS
1. Login to AWS free tier account or if not have a account then Create a free tier aws account.
2. Go to EC2 instances -> Click on Launch Instance
3. Name/tag give whatever you want in my case -> windows-server
4. Select AMI -> select windows AMI
   It will be something like - Microsoft windows server 2022 Base <- free tier
5. Select Instance type -> t2.micro <- free tier
6. Select Key pair if already have one
   or create new one if do not have one -> click on create new key pair,
   give a name - anything ex -> awskey, key pair type -> RSA, file format .pem <- create
7. Default VPC
8. Select Firewall (security groups) -> select existing security group -> select default (#later we need to add RDP rule in it if not have added)
9. Click on Launch Instance
10. Then go to security groups -> select default group -> click on inbound rule -> edit inbound rules
    Add rule -> type RDP , Source anywhere IPv4 -> save
11. Go back to instances - select the windows-server instance -> click on connect
12. Click on download remote desktop file -> keep -> open file
    Connect -> password (for this)
13. Go back to RDP client option of instance -> click on get password
14. Go to download folder and open the key file(.pem) we just created or the old one we had
    open it in notepad -> copy it ctrl+A and ctrl+c -> paste it to the ->
    private key contents -> click decrypt
    password generated -> copy that password and paste to -> #12 enter your credentials
    -> clik ok -> yes 
16. -- Successful to deply windows virtual machine --
