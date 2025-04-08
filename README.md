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
- Step 6: Practice with ChatGPT
- Step 7: Cleanup the lab



<h2>Project Walk-through:</h2>

<h3>Step 1: Login to osTicket</h3>
<p>
<img src="https://i.imgur.com/oatnDNZ.png" height="100%" width="100%" alt="Configuration step"/>
</p>
<p>
-Back in your Windows VM, navigate to Microsoft Edge and login to the admin/agent portal as the previously created osTicket agent account (whichever you created). In my case, I logged in as Daniel which I know is part of the support department and has View-only access.
Admin/agent Login Page: http://localhost/osTicket/scp/login.php.
</p>
<br />




<h3>Step 2: Create a troubleshooting ticket</h3>
<p>
<img src="https://i.imgur.com/fI6XrMH.png" height="100%" width="100%" alt="Configuration step"/>
</p>
<p>
-From within Microsoft Edge, open another tab and access the end-user portal at http://localhost/osTicket.

-From there, click on "Open a New Ticket", and then fill in the contact information using the previously created end-user information to create a troubleshooting ticket.
For example: 
- Help Topic: Report a Problem 
- Issue Summary: Network connectivity issue 
- Detailed explanation: Many of my employees are experiencing connectivity issues, it occurs at random time and has been consistent for many hours.
 (Cause IP conflict due to DHCP misconfig; requires Level II support)  
</p>
<br />




<h3>Step 3: Observe and set ticket properties</h3>
<p>
<img src="https://i.imgur.com/5JU59uX.png" height="100%" width="100%" alt="Configuration step"/>
</p>
<p>
-Back in the admin/agent panel, refresh the page and access the new ticket to observe its properties (Subject, Communications, Priority, Department, SLA, Assignation). Notice that I cannot make any changes to the ticket properties. Like mentioned previously, it's because I have View-only permissions on this agent account. The purpose of this is simply to show you what kind of access an agent configured with View-only has.
</p>
<br />


<p>
<img src="https://i.imgur.com/xEACRRQ.png" height="100%" width="100%" alt="Configuration step"/>
</p>
<p>
-To assign this ticket to the approptiate agent, go back to the admin account and assign it to "Level II Support" so that the other agent (may be different in your case), which is part of this team and is inherently considered more capable compared to the first agent, will be able to take charge and modify the ticket as needed. You can also specify a reason for this change of assignation (e.g., "Wide business impact due to network issue, assigning this ticket to Level II support Team").

-Additionally, change the SLA Plan to "Sev-A" instead of "Default SLA", and specify the reason for this change (e.g., "Wide impact, multiple users are experiencing intermittent network connectivity issues. Requires immediate attention.").
</p>
<br />




<h3>Step 4: Resolve the ticket</h3>
<p>
<img src="https://i.imgur.com/Vl9LN9C.png" height="100%" width="100%" alt="Configuration step"/>
</p>
<p>
-Logout from the current agent's account, and login as the other agent ("David" in my case).

-Access the ticket and assign it to the current agent's name.
You can also write a short message to specify that you will take charge of the ticket (e.g., "I'll be taking charge of this ticket").
</p>
<br />


<p>
<img src="https://i.imgur.com/NABiU3X.png" height="100%" width="100%" alt="Configuration step"/>
</p>
<p>
-From the ticket's properties page, you can also communicate findings and actions taken with other agents and/or end-users about the troubleshooting process. Proper documentation ensures transparency, continuity, and efficiency in resolving the issue. It helps agents track progress, prevents duplicate future efforts, and provides a clear history of troubleshooting steps. Additionally, keeping end-users informed improves communication and user satisfaction throughout the resolution process.

-As for the troubleshooting process for the network issue at hand, it was confirmed to be a DHCP server misconfiguration due to a limited subnet range that could not accommodate the growing number of users. As more devices joined the network, the DHCP server ran out of available IP addresses, leading to IP conflicts when multiple devices were assigned the same IP. This resulted in unstable connections as affected devices lost and regained network access intermittently.

Solution:
1) To resolve this issue, it was recommended to increase the subnet range (e.g., move from /24 to /23 if possible) to have more available IP addresses.
2) If expanding the subnet wasn't an option immediately, temporarily reducing the lease time while planning for a subnet expansion would have been another short-term solution.
</p>
<br />




<h3>Step 5:Mark the ticket as resolved</h3>
<p>
<img src="https://i.imgur.com/tnX8hAd.png" height="100%" width="100%" alt="Configuration step"/>
</p>
<p>
-Once the remediated issue has been confirmed with the impacted users, the agent can mark the ticket as resolved.
</p>
<br />




<h3>Step 6: Practice with ChatGPT</h3>
<p>
<img src="" height="100%" width="100%" alt="Configuration step"/>
</p>
<p>

</p>
<br />




<h3>Step :</h3>
<p>
<img src="" height="100%" width="100%" alt="Configuration step"/>
</p>
<p>

</p>
<br />




<h3>Step :</h3>
<p>
<img src="" height="100%" width="100%" alt="Configuration step"/>
</p>
<p>

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
