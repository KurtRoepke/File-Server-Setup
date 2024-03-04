<h1>Active Dicrectory Home Lab</h1>

 

<h2>Description</h2>
In this projectwe go over setting  up a file server to share files. we also set up permissons with group policy so certain department dont have access to documents they shouldnt see.<!-- Server manager, set permissios, make gpo's, <!--Server manager, gpo for permissions, gpo for map drives -->-->
<br />


<h2>Utilities Used</h2>

- <b>Server manager</b> 
- <b>Cmd</b>
- <b>Group policy </b>

<h2>Environments Used </h2>

- <b>Virtual Box</b> (21H2)
- <b>Windows 10 pro</b> (21H2)
- <b>Windows Server 2022</b> (21H2)

<h2>Program walk-through:</h2>

<!--go to server manager, tools, group policy management, .
<img src=images/.png" height="80%" width="80%"/>-->

<!--go to forest, domains right click the ou you want to add a new link gpo to and select create new gpo .
<img src=images/.png" height="80%" width="80%"/>-->

<!--go to the folder or drive you want to share right click and choose properties .
<img src=images/.png" height="80%" width="80%"/>-->

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


Start by going to the server manager and selecting add roles and features.
<img src="images/.png" height="80%" width="80%"/>

Next select file and storage services ,file and iscsi ,resorce manager and install.
<img src="images/.png" height="80%" width="80%"/>

After the computer has restarted .
<img src="images/.png" height="80%" width="80%" />

.
<img src="images/.png" height="80%" width="80%" />

.
<img src="images/.png" height="80%" width="80%" />
 
 .
<img src="images/.png" height="80%" width="80%" />
  
 .
<img src="images/.png" height="80%" width="80%" />

 . 
<img src="images/.png" height="80%" width="80%" or trianglead />
  
 .
<img src="images/.png" height="80%" width="80%" />
  
 .
<img src="images/1.png" height="80%" width="80%" />

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
