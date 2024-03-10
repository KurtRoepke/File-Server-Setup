<h1>Active Dicrectory Home Lab</h1>

 

<h2>Description</h2>
In this projectwe go over setting  up a file server to share files. we also set up permissons with group policy so certain department dont have access to documents they shouldnt see.<!-- Server manager, set permissios, make gpo's, <!--Server manager, gpo for permissions, gpo for map drives -->-->
<br />


<h2>Utilities Used</h2>

- <b>File explorer</b> 
- <b>Server manager</b> 
- <b>Cmd</b>
- <b>Group policy </b>

<h2>Environments Used </h2>

- <b>Virtual Box</b> (21H2)
- <b>Windows 10 pro</b> (21H2)
- <b>Windows Server 2022</b> (21H2)

<h2>Program walk-through:</h2>

First in order to enhance security we will set up new groups to keep files hidden from certain users go to server manager tools.
<img src="images/1.png" height="80%" width="80%"/>

click on active directory users and computers.
<img src="images/2.png" height="80%" width="80%" />

To make a new group right click the OU select new and choose group.
<img src="images/3.png" height="80%" width="80%" />

 Give the group a name and click ok.
<img src="images/4.png" height="80%" width="80%" />

To join users to a group right click the user and choose add to group .
<img src="images/5.png" height="80%" width="80%" />

Give the group a name and select ok.
<img src="images/6.png" height="80%" width="80%" />

Go to the file you want to share right click and choose properties.
<img src="images/7.png" height="80%" width="80%" />

 Select Security choose edit remove the domain users from the list and add group A to the list now only group A will see that file.
<img src="images/8.png" height="80%" width="80%" />
 
 Next go back to the server manager choose add roles and features file and storage services.
<img src="images/9.png" height="80%" width="80%"  />


 Choose file and iSCSI services and choose file server and server resource manager click next and install.
<img src="images/10.png" height="80%" width="80%" />


 Next go to file and storage services and go to shares menu.
<img src="images/11.png" height="80%" width="80%" />


 Right click the share box in the center of the menu and choose new share .
<img src=images/12.png" height="80%" width="80%"/>


choose smb quick and choose the drive or folder
<img src="images/13.png" height="80%" width="80%" />


 Remmeber the share path.
<img src="images/14.png" height="80%" width="80%" />

 Choose enable access-based enumeration to keep  share hiden from users that shouldnt see it choose next and create.
<img src="images/15.png" height="80%" width="80%" />

  
 Go to the network and sharing center in the control panel and choose advanced sharing settings.
<img src="images/16.png" height="80%" width="80%" />

 Make sure file and sharing is turned on on both the server and client machine. 
<img src="images/17.png" height="80%" width="80%" or trianglead />
  
 Go to the client machine go to programs and features in the control panel.
<img src="images/18.png" height="80%" width="80%" />
  
 select turn windows features on or off go to SMB and choose smb 1.0 client and turn it on.
<img src="images/19.png" height="80%" width="80%" />

 Go back to the server and make sure its alsoinstalled on the server go to add roles and features and choose smb server.
<img src="images/20.png" height="80%" width="80%" />

 Log  on to the user with permissions and go to file manager go to this pc and type in the folder path.
<img src="images/21.png" height="80%" width="80%" />

 This user has permissions so they can see the file.
<img src="images/22.png" height="80%" width="80%" />
 
 log on with the user without permissions they can see file b but file a is not visable because they dont have permissions.
<img src="images/23.png" height="80%" width="80%"  />

