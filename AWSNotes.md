## AWS NOTES
0. Accounts
    - Root user - This user will be created very first time when we create account
        - Root user have full permission to manage all services
        - Root user can create multiple users based on the need
        - Best practice is create IAM user and provide only required the access for the services
        - Can create account alias for IAM user to access the AWS console
          
    - IAM user - This user will have access based on the role has been associated
        - Access the console using Account alias or Using 12 account Id
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
   - Each regions will have 3 to 6 availability zones
   - Each are Isolated when one zone goes down other are accessable without any issues.
6. Password Policy
   - Password Policy is playing major role on password creation
   - If you want to more security for your account update your policies
   - This will help to set the policies like
         - Minimum password length
         - Expiry period
         - Previous Password reuse and so on..
7. MFA
   - Multi factor authentication is allow the user's accounts more secured
   - MFA can set up in various ways either virtually or physically
8. AWS Access tools
    - AWS services can accessed 3 different ways
          - Using AWS managment console https://console.aws.amazon.com
          - AWS CLI
          - AWS CloudShell
          - AWS SDK - This help to access the aws services for your application. This is language specific, based on the language which you working on you can download for that.
9. AWS CLI Configuration
      - User can download the AWS CLI for their OS Specific(Windows, Mac or Linux)
      - To access the AWS services via AWS ClI, User need access key.
      - User can generate the accesskey in user --> security credentials section.
      - Upon successfully creation of access key you will get the .CSV file with credentials
      - Configuration steps
            - Open command prompt and type 'aws configuration' and press enter
            - Enter 'Account Id', 'AccessKey','default region' and 'defaut output format'
10. Roles
    - Roles are created to provide the permission for the AWS services.
    - This is not going to be associated to any user. But this will be associated with any AWS service to access required stufs.
          - For example EC2 Instance wants to access any other AWS API/Service, it require roles.
          - When any service wants to access any other service it must require role permission
          - Role will have the permission are mapped like(Read, Write, Modify and so on..)
    
11. AWS Compute Options
    - Instances/Compute
    - Containers
      - Containers provide a standard way to package your application's code, configurations, and dependencies into a single object.
      - Containers run on top of the host OS and share the host's kernel. Each container running on a host runs its own isolated root     
        file system in a separate namespace that may include it’s own OS. They are designed to help ensure quick, reliable, and 
        consistent deployments, regardless of the environment.
      - Kubernetes is an open-source system for automating deployment, scaling, and management of containerized applications  
    - Serverless
    - Amazon EC2 are virtual server instances in the cloud.
    - Amazon ECS, Amazon EKS: Container management services that can run containers on either customer managed Amazon EC2 instances OR as 
      an AWS managed serverless offering running containers on AWS Fargate.
    - AWS Lambda is Serverless compute for running stateless code in response to triggers.
12. AWS Certified Solution Architect Associate.
    - This cource includes with 4 main domains knowledge
          - Design Secure Architecture
          - Design Resilient Architecture
          - Design High Performing Architeture
          - Design Cost Effective Architecture 

