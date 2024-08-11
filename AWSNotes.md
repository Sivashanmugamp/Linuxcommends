## AWS NOTES
0. Accounts
    - Root user - This user will be created the very first time when we create an account
        - Root users have full permission to manage all services
        - Root user can create multiple users based on the need
        - Best practice is to create an IAM user and provide only required access for the services
        - Can create an account alias for IAM user to access the AWS console
          
    - IAM user - This user will have access based on the role that has been associated
        - Access the console using an Account alias or Using 12 account ID
1. User Group
     - Users are aligned with the group
     - Policies/Permission are mapped with group 
2. Users
     - User will be created by Root user/IAM user
     - Requires User group to be associated  
3. Policies
       - User can create Policy/Permission
       - Need to provide the Action and Resources. 
4. Regions
    - Regions are available across the globe
    - Region has to be selected near to the client business area
    - All regions are not having all services
    - Nearest regions will avoid low latency issues. 
5. Availability Zones
   - Each region will have 3 to 6 availability zones
   - Each is Isolated when one zone goes down others are accessible without any issues.
6. Password Policy
   - Password Policy plays playing major role in password creation
   - If you want more security for your account update your policies
   - This will help to set the policies like
         - Minimum password length
         - Expiry period
         - Previous Password reuse and so on..
7. MFA
   - Multi-factor authentication allows the user's accounts more secured
   - MFA can be set up in various ways either virtually or physically
8. AWS Access tools
    - AWS services can accessed 3 different ways
          - Using AWS management console https://console.aws.amazon.com
          - AWS CLI
          - AWS CloudShell
          - AWS SDK - This helps to access the AWS services for your application. This is language specific, based on the language which you working on you can download for that.
9. AWS CLI Configuration
      - Users can download the AWS CLI for their OS Specific(Windows, Mac or Linux)
      - To access the AWS services via AWS CLI, User need an access key.
      - User can generate the access key in the user --> security credentials section.
      - Upon successfully creating of access key you will get the .CSV file with the credentials
      - Configuration steps
            - Open the command prompt type 'aws configuration' and press enter
            - Enter 'Account Id', 'AccessKey', 'default region' and 'default output format'
10. Roles
    - Roles are created to provide permission for the AWS services.
    - This is not going to be associated with any user. But this will be associated with any AWS service to access the required stuff.
          - For example, if EC2 Instance wants to access any other AWS API/Service, it requires roles.
          - When any service wants to access any other service it must require role permission
          - Role will have the permission mapped like(Read, Write, Modify and so on..)
    
11. AWS Compute Options
    - Instances/Compute
    - Containers
      - Containers provide a standard way to package your application's code, configurations, and dependencies into a single object.
      - Containers run on top of the host OS and share the host's kernel. Each container running on a host runs its own isolated root     
        file system in a separate namespace that may include its own OS. They are designed to help ensure quick, reliable, and 
        consistent deployments, regardless of the environment.
      - Kubernetes is an open-source system for automating the deployment, scaling, and management of containerized applications  
    - Serverless
    - Amazon EC2 are virtual server instances in the cloud.
    - Amazon ECS, Amazon EKS: Container management services that can run containers on either customer-managed Amazon EC2 instances OR as 
      an AWS-managed serverless offering running containers on AWS Fargate.
    - AWS Lambda is Serverless compute for running stateless code in response to triggers.
12. AWS Certified Solution Architect Associate.
    - This course includes 4 main domains of knowledge
          - Design Secure Architecture
          - Design Resilient Architecture
          - Design High Performing architecture
          - Design Cost Effective Architecture
13. How to access the EC2 instance in a Windows machine(https://chatgpt.com/c/447d28ec-01f0-416b-8120-d8307d411c1e)
    - To connect the EC2 instance we need .pem file.
    - When Launching a New EC2 Instance Key Pair Creation:
    - During the process of launching a new EC2 instance, AWS will prompt you to either create a new key pair or use an existing one.
    - If you create a new key pair, AWS will provide you with a .pem file to download. This is your private key, and it's crucial to
    - Download the .pem file immediately. You will not be able to download it later.
    - Save the .pem file in a secure location on your computer. You can later convert it to a .ppk file if you're using PuTTY on Windows.
    - If you don't have the .pem file, you cannot retrieve it from AWS after the key pair is created. In such cases, you would need to create a new key pair and associate it with a new instance or follow specific steps to replace the key pair (which involves creating a new instance or using existing EC2 features like instance recovery).
    - Converting .pem to .ppk (for PuTTY Users)
            -  If you plan to use PuTTY on a Windows machine, you'll need to convert the .pem file to a .ppk file using PuTTYgen:
            - Open PuTTYgen.
                    - Click on the Load button.
                    - Select the .pem file.
                    - Click the Save private key to save it as a .ppk file.
      - Accessing the Key File Later
        Once the instance is running, if you lose the key file (.pem or .ppk), you cannot download it again from AWS.
        If the key is lost and you can't connect to your instance, you may need to:
        Create a new key pair and manually attach it to your instance (this involves creating an AMI and launching a new instance from that AMI with a new key pair).
        - Use EC2 Instance Connect (available for certain instance types and AMIs) to temporarily access your instance without the key.
        - Use AWS Systems Manager (SSM) if it’s enabled on your instance, which allows you to connect to your instance without a key file.
       - Backup and Secure the Key File
        Always keep a backup of your .pem or .ppk file in a secure location, like a password-protected archive or a secure cloud storage service.


