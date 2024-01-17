<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br /><br />

This is a continuation of the [osTicket - Prerequisites and Installation Lab](https://github.com/andrewkhun/osticket-prereqs)<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- osTicket
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

1. Familiarity with the osTicket UI
2. Configure Roles, Departments, Teams, and Users
3. Configure Service Level Agreement (SLA) levels and Help Topics


<h2>osTicket UI</h2>
<p>
When navigating the osTicket User Interface (UI), note there are two panels: the Agent Panel and Admin Panel. You will know which panel you are on if the opposite panel is displayed on the top right of the UI. You will switch back and forth between the two panels during the post-configuration installation lab. 
  
In the photo below, you can see we are on the Agent Panel since the UI is displaying the Admin Panel as an option in the top right:
</p>
<p>
<img src="https://imgur.com/bV72KPM.png" height="70%" width="70%" alt="osTicket"/>
</p>


<h2>Configure Roles</h2>
<p>
  
To setup the proper osTicket configurations, you must log in with the 'user_admin' account that was created in the [osTicket - Prerequisites and Installation Lab](https://github.com/andrewkhun/osticket-prereqs)
</p>
<p>
Login using the account created.
</p>
<p>
<img src="https://imgur.com/0YfQFj8.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
Navigate to the Admin Panel, select Agents -> Roles, and click 'Add New Role'.
</p>
<p>
<img src="https://imgur.com/YekL3QB.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
We will create a new Role named 'Supreme Admin'. Once you have entered the name, select the 'Permissions' tab and ensure that all the permissions under the 'Tickets', 'Tasks', and 'Knowledgebase' tabs are checked to allow all permissions for this Role. Once all boxes have been checked, click 'Add Role'.
</p>
<p>
<img src="https://imgur.com/GBZ8gQy.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
<img src="https://imgur.com/BftSAif.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
<img src="https://imgur.com/liBmY8w.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
<img src="https://imgur.com/MpxDdQI.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
Once all boxes have been checked, click 'Add Role'.
</p>



<h2>Configure Deparments</h2>
<p>
To configure Departments, head to the Admin Panel then select Agents -> Departments, and click on 'Add New Department'.
</p>
<p>
<img src="https://imgur.com/FIknaQW.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
We will create a new department named 'System Administrators'. Once you have typed the name, click 'Create Dept'.
</p>
<p>
<img src="https://imgur.com/ftyyfpP.png" height="70%" width="70%" alt="osTicket"/>
</p>




<h2>Configure Teams</h2>
<p>
To configure Teams, head back to the Admin panel then go to Agents -> Teams, and click on 'Add New Team'. Create a new team called 'Level II Support', and add your current user account to the Team.
</p>
<p>
<img src="https://imgur.com/bWC5aor.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
<img src="https://imgur.com/xGbRUFS.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
Once done, click on 'Create Team'.
</p>





<h2>Configure Agents</h2>
<p>
To configure Agents or the ones who will be resolving the tickets, go to the Admin panel go to Agents -> Add New, and click on 'Add New Agent'.
</p>
<p>
<img src="https://imgur.com/cKtoFdN.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
Here we will create two new agents. The first Agent will be named 'jane doe' with the email 'jane.doe<span>@</span>osticket.com' and username 'jane.doe'. 
<p>
<img src="https://imgur.com/e7okRmE.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
Once you have set the proper information click on 'Set Password'. Uncheck the boxes 'Send the agent a password reset email' and 'Require password change at next login'. This will allow us to set the password to 'Password1' and enable us to use the password for our next login instead of requiring us to change it at the next login. 
</p>
<p>
<img src="https://imgur.com/WvkjIeB.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
Click on the 'Access' tab and select the 'System Administrators' department with the role of 'Supreme Admin'. For 'Extended Access', add the 'Support' department and 'Supreme Admin' role as well. In the 'Teams' tab, select the 'Level II Support' team and click 'Add'.
</p>
<p>
<img src="https://imgur.com/aLLJRoN.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
Finally, click on 'Save Changes' to create a new Agent. 
</p>
<p>
<img src="https://imgur.com/XkHoEHJ.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
We will create a second Agent with the name 'john smith'. The creation process is similar to the previous Agent creation process with just a few changes. Ensure the user's name, email, username, and password are properly set. 

In the 'Access' tab, set the 'Primary Department' to 'Support' and the role to 'Supreme Admin'.

Next, in 'Teams' add the 'Level I Support' team, then click Save changes.
</p>
<p>
<img src="https://imgur.com/ahYOo13.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
<img src="https://imgur.com/tr1GKHu.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
<img src="https://imgur.com/sRUx8p6.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
Please note, when configuring a true work/production environment osTicket instance, ensure that you apply the concept of 'Least Privilege' to only provide the least amount of access a user needs to complete their duties. However, for the sake of this lab, we will allow john smith to have a 'Supreme Admin' role.
</p>




<h2>Configure Users</h2>
<p>
To configure Users who will submit tickets into the osTicket system, navigate to the Agent panel then click on Users -> Add New. Here we will create two new Users.
</p>
<p>
<img src="https://imgur.com/d75tPfh.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
Our two new users will be 'karen karen' with the email 'karen<span>@</span>osticket.com' and 'ken ken' with the email 'ken<span>@</span>osticket.com'. Once you have entered the proper information for each user, click on 'Add User'.
</p>
<p>
<img src="https://imgur.com/OV9Lf0p.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
<img src="https://imgur.com/uppLFPo.png" height="70%" width="70%" alt="osTicket"/>
</p>



<h2>Allow Anyone to Create Tickets</h2>

<h2>Configure SLA Levels</h2>

<h2>Configure Help Topics</h2>
