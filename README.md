# aws-cli-configure
To install the AWS CLI on your Ubuntu EC2 instance, follow these steps:

1. Update Your Package Repository
First, make sure your package list is up to date:


sudo apt-get update
2. Install Dependencies
Install the required dependencies for the AWS CLI installation:


sudo apt-get install -y unzip curl
3. Download the AWS CLI v2 Installer
Next, download the latest version of the AWS CLI v2:


curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
4. Unzip the Installer
Unzip the downloaded file:


unzip awscliv2.zip
5. Run the Installer
Now, install the AWS CLI:


sudo ./aws/install
6. Verify the Installation
After the installation is complete, verify that AWS CLI is installed by checking the version:


aws --version
You should see output similar to:


aws-cli/2.x.x Python/3.x.x Linux/4.x.x
7. Configure the AWS CLI
Finally, configure the AWS CLI with your AWS Access Key ID, Secret Access Key, and default region:


aws configure
You will be prompted to enter:

AWS Access Key ID: Your access key.
AWS Secret Access Key: Your secret key.
Default region name: e.g., us-east-1.
Default output format: You can use json or text.
Optional Step: Enable Auto-Completion (Optional)
To enable AWS CLI auto-completion (so you can use tab to complete commands), run the following command:


complete -C '/usr/local/bin/aws_completer' aws
Now you should be able to use AWS CLI on your EC2 instance!
