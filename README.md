# Integrating-Amazon-RDS-with-WordPress

Step1: Create Amazon EC2 with amazon linux 2 AMI

Step2: Connect ec2 to terminal.

         sudo su -
 
         yum install httpd -y

         systemctl start httpd
 
         systemctl enable httpd
         
         We can check wheather our service is running or not by
         
         system status httpd
         
Step3: Next, Create RDS By default VPC with Configuration which given in images.

Step4: Install php in Ec2

       amazon-linux-extras install -y php7.2
       
Step5: Now, Download Wordpress and Unzip the file.

       wget http://wordpress.org/latest.tar.gz
       
       tar -xvzf latest.tar.gz
       
Step6: Copy all files in folder of Apache Web Server So that it can access the files by html
  
       cp -rf wordpress/* /var/www/html
       
       We can check our file by "ls"
       
Step7: Install MySQL in CMD
       
       yum install mysql -y
       
Step8: Copy the public Ip of instance and paste it in browser
    
       http://IP/
       
Step9: A page will appear in browser if the all upper configuration is right.Fill all the Credentials like username, password, database name and in database host fill the endpoint of Rds.

Step10: If all the process are good then one other page of code will appear for "run as installation".

Step11: Create new file in ec2 of name "wp-config.php file" and paste the code in this file which appear in our previous page.

Step12: After Saving the file go to the Browser and click "run as installation".

Step13: Fill all the details, click submit option and download the Wordpress.

Step14: Finally Login the Account Credentials and setup wordpress account.

# Problem Facing
 
 Add mysql/Arura in inbound rule in Default security group which is attach to rds.
 
 Add Htttp in inbound rule in security group which is attach to ec2.

 

 
