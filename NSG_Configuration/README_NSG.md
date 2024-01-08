
# Azure Network Security Groups (NSGs) Implementation and Troubleshooting

This project was focused on mastering Azure Network Security Groups (NSGs) to manage and secure network traffic for my Azure Virtual Machine (VM), AZ-VM. The journey involved configuring NSG rules to allow specific traffic and deny others, such as HTTP, SSH, and blocking FTP, and troubleshooting various challenges along the way.


## OBJECTIVES

- Implement NSGs to control network traffic to and from AZ-VM.
- Enable and test HTTP and SSH access to AZ-VM.
- Overcome connectivity issues through troubleshooting.
- Block and verify the blocking of FTP traffic.
## PROCESSES AND CHALLENGES

##Configuring NSGs for Traffic Management
-Action: Created an NSG named WebServerNSG in Azure, specifying rules to allow HTTP (port 80) and SSH (port 22) traffic, and block others like FTP (port 21).

WebServerNSG inbound rules list 
![App Screenshot](https://via.placeholder.com/468x300?text=App+Screenshot+Here)

ALso Az-VM 's networking section(showing ports allowed or disallowed)
![App Screenshot](https://via.placeholder.com/468x300?text=App+Screenshot+Here)

Added WebServerNSG to the Subnet of Virtual Machine (Az-VM)
![App Screenshot](https://via.placeholder.com/468x300?text=App+Screenshot+Here)


## Allowing and Testing HTTP Access
- Action: Set up HTTP access to AZ-VM and verified it.
Steps:
1) Configured VM Firewall: Added an inbound rule on the VM's firewall to allow traffic on port 80.
2) Installed IIS Web Server: Set up IIS on AZ-VM to host a web service.
3) Verified Port Accessibility: Installed Telnet on my local computer and used it to confirm that port 80 was open.
4) Browser Test: Accessed http://20.106.204.88 from my web browser, which initially failed to load the VM's default webpage.
5) Troubleshooting: Realized the need to adjust WebServerNSG settings and VM's firewall to allow HTTP traffic properly.
- Outcome: Successfully accessed the VM's web service via HTTP after adjustments.

![App Screenshot](https://via.placeholder.com/468x300?text=App+Screenshot+Here)

## Enabling and Troubleshooting SSH Access
- Action: Configured and tested SSH access to AZ-VM.
- Challenges:
1) Connection Timed Out: Encountered when trying to SSH into the VM.
- Solution: Checked and adjusted WebServerNSG settings to allow traffic on port 22 and confirmed the VM's public IP address and running status.
2) Connection Refused: Faced after WebServerNSG adjustments.
- Solution: 1) Ensured the OpenSSH server was installed and running on the VM.
2) Configured Windows Firewall to allow SSH traffic.
3) Reverified WebServerNSG configurations in Azure.
- Outcome: Successfully established an SSH connection to AZ-VM after resolving these issues.

![App Screenshot](https://via.placeholder.com/468x300?text=App+Screenshot+Here)
![App Screenshot](https://via.placeholder.com/468x300?text=App+Screenshot+Here)

## Blocking and Testing FTP Access
- Action: Set up NSG rules to block FTP traffic and conducted tests to confirm the blockage.
- Steps:
1) NSG Configuration: Added a rule in NSG to deny inbound FTP traffic (port 21).
2) Testing Blockage: Attempted to connect to the VM using an FTP client.
3) Observation: The connection attempt failed, indicating the effectiveness of the NSG rule in blocking FTP access.
- Outcome: Confirmed that FTP traffic was successfully blocked by the NSG, enhancing the security of my Azure environment.

![App Screenshot](https://via.placeholder.com/468x300?text=App+Screenshot+Here)
## LESSON LEARNED

- Gained practical experience in configuring Azure NSGs for different traffic types.
- Learned the intricacies of setting up and troubleshooting SSH on a Windows VM.
- Developed skills in diagnosing and resolving network connectivity issues.
- Understood the importance of NSG rules in blocking unwanted traffic like FTP.

## FUTURE PLANS

- Plan to explore more advanced features in Azure networking and security.
- Intend to automate monitoring and manage network security more proactively.

## CONCLUSION

This project was a comprehensive exercise in Azure network security. I navigated through various technical challenges, enhancing my understanding of NSGs and their impact on VM connectivity and security. Each problem faced was an opportunity to deepen my knowledge and troubleshooting skills in Azure.