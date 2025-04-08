# <p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" height="100%" width="100%" alt="Setting Up in Azure"/>
<br />

<h1>osTicket - End-User Ticketing & Helpdesk Resolution</h1>

<h2>Description</h2>
In this guided lab, we will simulate real-world helpdesk interactions by experiencing both creating an end-user troubleshooting ticket and acting as a helpdesk agent resolving it.<br/>
<br/>

<h2>Environments and Technologies</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop Connection
- osTicket


<h2>Operating Systems Used </h2>

- Windows 10 Pro, version 22H2


<h2>High-Level Steps</h2>

- Step 1: Login to osTicket
- Step 2: Create a ticket
- Step 3: Observe and set ticket properties
- Step 4: Resolve the ticket 
- Step 5: Mark the ticket as resolved 
- Step 6: Create and resolve another ticket
- Step 7: Cleanup the lab



<h2>Project Walk-through:</h2>

<h3>Login to osTicket</h3>
<p>
<img src="https://i.imgur.com/oatnDNZ.png" height="100%" width="100%" alt="Configuration step"/>
</p>
<p>
-Back in your Windows VM, navigate to Microsoft Edge and login to the admin/agent portal as the previously created osTicket agent account (whichever you created). In my case, I logged in as Daniel which I know is part of the support department and has View-only access.
Admin/agent Login Page: http://localhost/osTicket/scp/login.php.
</p>
<br />




<h3>Step 7: Cleanup the lab</h3>
<p>
<img src="https://i.imgur.com/Alt4mSy.png" height="100%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
-Back in Azure, type "Resource groups" in the search and delete the Resource Group created at the beginning of this lab (if you see a second one, delete it too). Your VMs will be deleted subsequently because they are part of the Resource Group.
</p>
<br />




<p>
<img src="https://i.imgur.com/s3gHEyF.png" height="100%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
-Verify Resource Groups deletion to ensure that no resources are left behind, preventing unnecessary costs and resource consumption. 




<h2>End-User Ticketing & Helpdesk Resolution process in now complete!</h2>

<b>We've successfully gone through the life cycle of a ticket from creation to resolution, made changes to the tickets when necessary like assigning the tickets, changing the SLA (Service Level Agreement), commenting to create a thread of clear communication, as well as practicing with different ticket scenarios.</b>
<br />
<br />
</p>
