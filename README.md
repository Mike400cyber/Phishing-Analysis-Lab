<h1>Phishing-Analysis-Challenge</h1>

<h2>Description</h2>
A user has received a phishing email and forwarded it to the SOC. Can you investigate the email and attachment to collect useful artifacts?
<br />

<h2>Environments Used </h2>

- <b>BlueTeamLabs.online</b> 

<h2>Lab walk-through:</h2>

<p align="center">
Who is the primary recipient of the email? <br/>
<img src="https://imgur.com/Rb96HWR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<h2></h2>
<p align="center">
What is the original IP? <br/>
<br /> 
<img src="https://imgur.com/AuFlsrS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<h2></h2>
<p align="center">
Perform reverse DNS on this IP address, what is the resolved host? (whois.domaintools.com) <br/>
<br />
<img src="https://imgur.com/fibqbTe.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br /> 
<br />
<br />
<h2></h2> 
<p align="center">
Change directory permissions: Remove "group" write permissions for the drafts directory<br/>
<img src="https://imgur.com/cR0VnFM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<h2>chmod command (Change directory permissions):</h2>
<br />
I used the ls -la command to examine the detailed permissions of files and directories, identifying that the group had write permissions in the "drafts" directory.
I used the chmod command to remove write permissions from the group. The "researcher2" user already had access and write permissions so the chmod g-x drafts command was used to remove write permissions.
<h2>Summary:</h2>
In this project, I was tasked with updating file and directory permissions within the "projects" directory to align with the organization's security and authorization requirements. I began by using the ls -l and ls -la command to perform a detailed audit of the current file and directory permissions. This step was crucial in assessing the existing permission settings and identifying where changes were needed.
Based on the results, I used the chmod command to modify the permissions on multiple files and directories. This ensured access levels were appropriately set to enhance security while meeting the organization's authorization standards.
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
