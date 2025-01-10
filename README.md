# Automating-Active-Directory-with-Powershell

<h2>Description</h2>
  Automating Active Directory (AD) with PowerShell simplifies administrative tasks like creating, modifying, and deleting users, groups, and computers, managing permissions, resetting passwords, generating reports, and automating repetitive processes such as user provisioning. This approach reduces manual effort, improves accuracy, boosts efficiency, and enables complex tasks to be performed with ease while offering better control and visibility. Key PowerShell cmdlets like Get-ADUser, Set-ADUser, Get-ADGroup, New-ADGroup, and Import-Csv streamline AD management, making it faster, consistent, and more reliable.

 
  RSAT (Remote Server Administration Tools) were used to allow remote commands to active directory via powershell. This project consisted of a csv file of employees' info being imported via powershell, as well as any users that were already in active directory. When the two groups of users were compared one could tell which users/employees needed to be created, synced, or removed. Users were created, usernames were generated. Users that already existed were synced and updated if need be. Users that had been "fired" were removed from the active directory. Functions were created with different parameters. These functions would allow the -Get commands to receive data from AD. The functions included an array of hashtables, which contained the objects in expression. Commands involved creating a new user, removing a user, and syncing users already created vs the new ones being created. 

<h2>Things Learned/Troubleshooting</h2>
Various errors after entering commands were receieved and I found that it was due to things such as:
  running a function first in order for a commmand to work via powershell,
  delegating control to the admin account on the domain controller,
  removing implicit deny permissions
to en
I was able to fix these errors within active directory. 

<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b>
- <b>Remote Server Administration Tools</b>

<h2>Environments Used </h2>

- <b>Windows Server 2019</b>
 - <b>Active Directory</b>
  
<h2>Program walk-through:</h2>

Code wrriten via powershell with the purpose of automating active directory. 

![VirtualBox_DC_09_01_2025_23_29_56](https://github.com/user-attachments/assets/2f9a26ff-8f8a-4a5c-8de1-c33bd4e13667)

Delegating control to the administrator on the domain controller helped with the issues I had during this lab, in which certain commands wouldn't work due to 'access being denied.'

![VirtualBox_DC_25_09_2024_16_21_46](https://github.com/user-attachments/assets/88a76186-6709-4783-ba2b-3f4bbe890c2a)

After validating the OU and running functions, the create-newuser command was able to be used via powershell and created new users in active directory. 

![Screenshot 2025-01-05 180744](https://github.com/user-attachments/assets/2b921d7b-51d3-42b5-814a-5af36df1aad1)

Commands were used to display different data, which in this case is users that have been removed from the OU due to being "fired." 

![Screenshot 2025-01-05 181751](https://github.com/user-attachments/assets/3852b54b-ecf8-414f-bd99-7501267c332a)

Organization Units (OUs) within Active Directory allows you to group objects such as user accounts. Adminstrators can be assigned to specific OUs and can apply group policy for certain configuration settings. 
![Screenshot 2025-01-05 175536](https://github.com/user-attachments/assets/91e2845b-6912-4684-8d1a-14f9ef6c8790)
![VirtualBox_DC_09_01_2025_23_29_56](https://github.com/user-attachments/assets/2f9a26ff-8f8a-4a5c-8de1-c33bd4e13667)
