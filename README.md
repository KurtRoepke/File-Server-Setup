<h1>File server setup</h1>

 

<h2>Description</h2>
<!--In this projectwe go over setting  up a file server to share files. we also set up permissons with group policy so certain department dont have access to documents they shouldnt see.<!-- Server manager, set permissios, make gpo's, <!--Server manager, gpo for permissions, gpo for map drives -->-->
<br />-->


<h2>Utilities Used</h2>

- <b>File explorer</b> 
- <b>Server manager</b> 
- <b>Active Directory </b>

<h2>Environments Used </h2>

- <b>Virtual Box</b> (21H2)
- <b>Windows 10 pro</b> (21H2)
- <b>Windows Server 2022</b> (21H2)

<h2>Program walk-through:</h2>

First in order to enhance security we will set up new groups to keep files hidden from certain users go to server manager tools.
<img src="Images/1.png" height="70%" width="70%"/>



click on active directory users and computers.
<img src="Images/2.png" height="70%" width="70%" />



To make a new group right click the OU select new and choose group.
<img src="Images/3.png" height="70%" width="70%"  />



 Give the group a name and click ok.
<img src="Images/4.png" height="70%" width="70%" />


 
 To join users to a group right click the user and choose add to group .
<img src="Images/5.png" height="70%" width="70%"  />



Enter the group name and add it to the list of permissions.
<img src="Images/6.png" height="70%" width="70%"  />



Go to the file you want to share right click and choose properties.
<img src="Images/7.png" height="70%" width="70%"  />



Select Security choose edit remove the domain users from the list and add group A to the list now only group A will see that file.
<img src="Images/8.png"  height="70%" width="70%"  />

 
  
Next go back to the server manager choose add roles and features file and storage services.
<img src="Images/9.png" height="70%" width="70%"    />



Choose file and iSCSI services and choose file server and server resource manager click next and install.
<img src="Images/10.png" height="70%" width="70%"  />



Next go to file and storage services and go to shares menu.
<img src="Images/11.png"  height="70%" width="70%"  />



Right click the share box in the center of the menu and choose new share .
<img src="Images/12.png" height="70%" width="70%"  />



Choose smb quick and choose the drive or folder you want to share.
 <img src="Images/13.png"  height="70%" width="70%"  />



This is the path to the network share.
<img src="Images/14.png"  height="70%" width="70%"  />



Choose enable access-based enumeration to keep  share hiden from users that shouldnt see it choose next and create.
<img src="Images/15.png"  height="70%" width="70%"  />

  

Go to the network and sharing center in the control panel and choose advanced sharing settings.
<img src="Images/16.png"  height="70%" width="70%"  />



Make sure file and sharing is turned on on both the server and client machine. 
<img src="Images/17.png" height="70%" width="70%"  />
  
 

Go to the client machine go to programs and features in the control panel.
<img src="Images/18.png" height="70%" width="70%"  />
  
 

Select turn windows features on or off go to SMB and choose smb 1.0 client and turn it on.
<img src="Images/19.png"  height="70%" width="70%"  />



Go back to the server and make sure its alsoinstalled on the server go to add roles and features and choose smb server.
<img src="Images/20.png" height="70%" width="70%" />



Log  on to the user with permissions and go to file manager go to this pc and type in the folder path.
<img src="Images/21.png" height="70%" width="70%" />

 

This user has permissions so they can see the file.
<img src="Images/22.png" height="70%" width="70%" />
 


log on with the user without permissions they can see file b but file a is not visable because they dont have permissions.
<img src="Images/23.png" height="70%" width="70%"  />

