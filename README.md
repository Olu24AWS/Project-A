# Assignment Steps to launch my First EC2 Instance  
## Step 1: Sign Up for AWS
If you haven’t already, you’ll need to create an AWS account at aws.amazon.com. You’ll need to provide some basic information and payment details, as AWS charges based on the resources you use.

## Step 2: Create an IAM User
Sign in to the AWS Management Console as the root user.
Go to the IAM (Identity and Access Management) page.
Create a new IAM user with administrative permissions. This is a best practice for managing AWS services securely.
## Step 3: Launching an EC2 Instance
Log into AWS Management Console: Use your IAM user credentials to sign in.
Navigate to EC2 Dashboard: Go to Services and select EC2 to open the EC2 Dashboard.
Launch Instance: Click on the “Launch Instance” button to start the process.
Choose an AMI (Amazon Machine Image): Select an AMI that serves as the template for your instance. AWS provides several AMIs with different configurations of operating systems and software.
Select an Instance Type: Choose the type of instance based on your needs. For basic applications, a "t2.micro" instance may suffice and is eligible for the free tier.
Configure Instance: Configure details like network, IAM role, and shutdown behavior. You can leave most settings at their defaults for a simple test.
Add Storage: Adjust the size and type of storage. The default SSD should be fine for most basic purposes.
Tag Instance: Add tags by creating a Name tag with a value that helps you identify your server.
Configure Security Group: Set up firewall rules that control traffic to your instance. For a web server, you might allow TCP on port 80 (HTTP) and 443 (HTTPS).
Review: Check your settings. If everything looks correct, click “Launch”.
## Step 4: Create and Download Key Pair
Upon launching, you’ll be prompted to select an existing key pair or create a new one. If you don’t have one, choose “Create a new key pair”.
Name your key pair and download it. Keep this file secure; it’s your private key to access the instance.
## Step 5: Connect to Your Instance
After the instance launches, select it in the console to view its details.
Find the “Public DNS (IPv4)” or “IPv4 Public IP”.
Connect using an SSH client:
For Windows users, you can use PuTTY or any SSH client. Convert the .pem key to .ppk using PuTTYgen if necessary.
For macOS/Linux users, set the correct permissions for the key file (chmod 400 your-key-name.pem) and connect using:
bash
Copy code
ssh -i /path/to/your-key-name.pem ec2-user@your-instance-public-dns
Replace ec2-user with the appropriate username based on the AMI (e.g., ubuntu for Ubuntu servers).
## Step 6: Manage Your Instance
Once connected, you can configure and use your server according to your needs.
Monitor your instance via the EC2 dashboard to keep track of its status and usage.
## Step 7: Terminate Your Instance
When you no longer need your instance, be sure to terminate it through the EC2 dashboard to stop incurring charges. Simply select the instance, go to Actions -> Instance State -> Terminate.
Launching an AWS EC2 instance might seem complex at first, but it becomes straightforward with a bit of practice. This guide should help you get started smoothly!






