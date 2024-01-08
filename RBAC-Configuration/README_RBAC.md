
# Configure Role-Based Access Control (RBAC) for Azure Resources

In this project, I took on the challenge of enhancing our Azure environment's security by diving into Role-Based Access Control (RBAC). My goal was to understand and implement custom roles, particularly focusing on a "VM Operator" role.


## Resources

- Azure VM 'AZ-VM': Created this VM as a key part of my project.
- Storage 'techsolconfidential': Set up for secure data storage.
- Using 'TechSoultions' Resource Group: This was the home base for my project.
- Within 'Azure subscription 1': My playground for RBAC setup.

## Roles

- 'VM Operator' Role: Designed to give 'IT ADMIN' precise control over the 'AZ-VM'.
- 'Reader' Role: Assigned to 'REGULAR EMPLOYEE' for safe viewing access to our storage account.
## STEPS FOLLOWED

- Writing the Role in JSON: This was where I defined what a 'VM Operator' can do.

- Overcoming Cloud Shell Issues: Had a bit of a struggle with accessing the JSON file in Azure Cloud Shell, but managed to upload it directly.

- Creating the Role in Azure: Ran into a 'Conflict' error at first, which I resolved by checking with Get-AzRoleDefinition
## CHALLENGES

- Uploading to Cloud Shell: Initially couldn't access my local JSON file in Cloud Shell. Solution: Uploaded it directly, which worked!

- Dealing with a 'Conflict' Error: Turns out the 'VM Operator' role already existed. I used Get-AzRoleDefinition to figure this out
## TESTING THE ROLES

- As 'IT ADMIN': I was able to start and stop 'AZ-VM' but couldn’t create or delete it – just as planned.

- As 'REGULAR EMPLOYEE': Verified that they could only view details in 'techsolconfidential' and nothing more
## LEARNINGS

I gained valuable hands-on experience with Azure's RBAC, sharpening my skills in cloud security. I learned the importance of precise role assignments and how to navigate Azure's environment, especially the Cloud Shell.
## Screenshots

JSON Role Definition:
![App Screenshot](https://github.com/SarthakRana007/Azure-AD-Identity-Management/blob/d7f6d59106ff5eef770efc16feb513c926413d39/RBAC-Configuration/Screenshots/1.png)
![App Screenshot](https://github.com/SarthakRana007/Azure-AD-Identity-Management/blob/d7f6d59106ff5eef770efc16feb513c926413d39/RBAC-Configuration/Screenshots/1.1.png)
![App Screenshot](https://github.com/SarthakRana007/Azure-AD-Identity-Management/blob/d7f6d59106ff5eef770efc16feb513c926413d39/RBAC-Configuration/Screenshots/1.2.png)

Role Assignment in Azure Portal:

IT Admin(User) assigned the role VM OPERATOR.
![App Screenshot](https://github.com/SarthakRana007/Azure-AD-Identity-Management/blob/d7f6d59106ff5eef770efc16feb513c926413d39/RBAC-Configuration/Screenshots/2.png)

Regular Employee(User) assigned the role READER.
![App Screenshot](https://github.com/SarthakRana007/Azure-AD-Identity-Management/blob/d7f6d59106ff5eef770efc16feb513c926413d39/RBAC-Configuration/Screenshots/3.png)


Testing as Different Users:
Signed in as IT Admin and able to run Virtual Machine AZ-VM.
![App Screenshot](https://github.com/SarthakRana007/Azure-AD-Identity-Management/blob/e800ca55828da9d887b3158a0627dfd0c155b84d/RBAC-Configuration/Screenshots/4.png)

IT Admin not authorized to create or delete VM
![App Screenshot](https://github.com/SarthakRana007/Azure-AD-Identity-Management/blob/e800ca55828da9d887b3158a0627dfd0c155b84d/RBAC-Configuration/Screenshots/5.png)

Regular Employee assigned as Reader for Storage account TechSolConfidential not authorized to configure settings.
![App Screenshot](https://github.com/SarthakRana007/Azure-AD-Identity-Management/blob/e800ca55828da9d887b3158a0627dfd0c155b84d/RBAC-Configuration/Screenshots/6.png)


