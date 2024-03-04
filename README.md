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

First go to the folder or drive you want to share and select properties .
<img src="images/1new.png" height="80%" width="80%" />

Next select security add users or groups and select add and add the users or groups that need to see the share and choose there permissions.
<img src="images/2.png" height="80%" width="80%" />

<!--go to server manager select add roles and features choose file and storage then file and iSCSI and finaly file server and install.
<img src=images/3.png" height="80%" width="80%"/>-->

<!--Next go to the left side of the server manager and select file and storage and shares.
<img src=images/4.png" height="80%" width="80%"/>-->

<!-- Right click the share box in the center of the menu and choose new share .
<img src=images/5.png" height="80%" width="80%"/>-->

Select SMB quick and choose enable access-based enumeration so files stay hidden from users who dont need to see them .
<img src="images/6.png" height="80%" width="80%" />

<!-- restart machine -->

<!--.
<img src=images/.png" height="80%" width="80%"/>-->
<!-- 
    Active Directory setup
Company location
        group for map drive
                    test ou
                       group
                    test ou
                       group       -->


go to the server manager and choose tools and group policy management.
<img src="images/7.png" height="80%" width="80%"/>

.right click the ou you want to link the gpo to and choose create new gpo.
<img src="images/8.png" height="80%" width="80%"/>

 Right click the GPO and choose edit.
<img src="images/9.png" height="80%" width="80%" />

Next go to user config, prefrences, windows settings and drive maps.
<img src="images/10.png" height="80%" width="80%" />
 
 .
<img src="images/11.png" height="80%" width="80%" />
  
 Go to the network and sharing center in the control panel and choose advanced sharing settings.
<img src="images/12.png" height="80%" width="80%" />

 Make sure file and sharing is turned on on both the server and client machine. 
<img src="images/13.png" height="80%" width="80%" or trianglead />
  
 Go to the client machine go to programs and features in the control panel.
<img src="images/14.png" height="80%" width="80%" />
  
 select turn windows features on or off go to SMB and choose smb 1.0 client and turn it on.
<img src="images/15.png" height="80%" width="80%" />

 .
<img src="images/newpic.png" height="80%" width="80%" />

 .
<img src="images/routing.png" height="80%" width="80%" />

 .
<img src="images/3.png" height="80%" width="80%" />
 
 .
<img src="images/4.png" height="80%" width="80%"  />

 .
<img src="images/dhcpc.png" height="80%" width="80%" />

 .
<img src="images/scope.png" height="80%" width="80%" />

 .
<img src="images/addr.png" height="80%" width="80%" />

 .
<img src=" images/5.png " height="80%" width="80%" />

 .
<img src="images/6.png" height="80%" width="80%" />

 .
<img src="images/7.png" height="80%" width="80%" />

 . 
<img src="images/8.png" height="80%" width="80%" />
