
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

![App Screenshot](https://via.placeholder.com/468x300?text=App+Screenshot+Here)

