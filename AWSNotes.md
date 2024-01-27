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
   - Each are Isolated when one zone goes down other are accessable without any issues
    
   

