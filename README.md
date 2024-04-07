FLOW OF EXECUTION


1. Login to AWS Account:
   - Open your web browser and navigate to the AWS Management Console.
   - Enter your AWS account credentials (username and password) to log in.

3. Create Key Pairs:
   - Go to the EC2 service dashboard in the AWS Management Console.
   - Navigate to the Key Pairs section.
   - Click on the "Create Key Pair" button.
   - Provide a name for the key pair and then click "Create Key Pair".
   - This will generate a new key pair consisting of a public key and a private key, which you will use to securely access your EC2 instances.

4. Create Security Groups:
   - In the EC2 service dashboard, navigate to the Security Groups section.
   - Click on the "Create Security Group" button.
   - Provide a name and description for the security group.
   - Define the inbound and outbound rules to control the traffic allowed to and from your instances.
   - Click "Create Security Group" to create the security group.

5. Launch Instances with User Data:
   - Navigate to the EC2 service dashboard.
   - Click on the "Launch Instance" button.
   - Select the desired Amazon Machine Image (AMI) for your instances.
   - Choose the instance type, configure instance details, add storage, configure security groups, and add tags as necessary.
   - In the "Configure Instance Details" section, you can provide user data scripts to be executed during instance launch.
   - Review your configuration and then launch the instance.

6. Update IP to Name Mapping in Route 53:
   - Go to the Route 53 service dashboard.
   - Select the hosted zone corresponding to your domain.
   - Create or edit DNS records (such as A records or CNAME records) to map IP addresses to domain names or subdomains.

7. Build Application from Source Code:
   - Set up a development environment with the necessary tools and dependencies.
   - Clone or download the source code of your application from a version control system like Git.
   - Build the application using the appropriate build tools and commands.

8. Upload Artifacts to S3 Bucket:
   - Go to the S3 service dashboard.
   - Create a new S3 bucket if necessary.
   - Upload the built artifacts (e.g., WAR files, JAR files, or any other binaries) to the S3 bucket.

9. Download Artifacts to Tomcat EC2 Instance:
   - SSH into the Tomcat EC2 instance using the private key generated earlier.
   - Install any required tools or dependencies if not already installed.
   - Download the artifacts from the S3 bucket to the Tomcat EC2 instance.

10. Setup ELB with HTTPS:
   - Navigate to the EC2 service dashboard.
   - Create a new Elastic Load Balancer (ELB) and configure it with HTTPS listeners.
   - Associate the ELB with the EC2 instances running your application.
   - Configure SSL certificates for HTTPS communication.

11. Map ELB Endpoint to Website Name in GoDaddy:
    - Log in to your GoDaddy account.
    - Navigate to the domain management section.
    - Edit the DNS settings to add a new CNAME record pointing to the ELB endpoint.

12. Verify:
    - Ensure that the application is accessible via the domain name mapped to the ELB endpoint.
    - Test the application to verify that it functions correctly.

13. Build Autoscaling Group for Tomcat Instance:
    - Navigate to the EC2 service dashboard.
    - Create a new Autoscaling Group and configure it to scale based on metrics such as CPU utilization or request count.
    - Associate the Autoscaling Group with the existing EC2 instances running your Tomcat application.
    - Set up scaling policies to automatically add or remove instances based on demand.
