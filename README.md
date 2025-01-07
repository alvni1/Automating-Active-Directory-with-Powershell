# Automating-Active-Directory-with-Powershell

<h2>Description</h2>
Project consisted of: 
A csv file of employee info was imported via powershell, as well as the employees in AD. The two were compared, and you could see which employees needed to be created, synced, or removed. Users were created, usernames were generated. Users that already existed were synced and updated if need be. Users that had been "fired" were removed from the AD. RSAT (Remote Server Administration Tools) were used to allow remote commands via powershell. -Get commands were used to retrieve different types of data. Functions were created with different parameters. These functions would allow the -Get commands to receive datat from AD. The functions included an array of hashtables, which contained the objects in expression. Commands involved creating a new user, removing a user, and syncing users already created vs the new ones being created. 

Things learned/Troubleshooting:
-Must run the function first in order for it to work in the command line via powershell
-


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 


<h2>Environments Used </h2>

- <b>Windows Server 2019</b>
 - <b>Active Directory</b>
  
<h2>Program walk-through:</h2>
