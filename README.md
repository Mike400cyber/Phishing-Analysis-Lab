<h1>Phishing-Analysis-Lab</h1>

<h2>Description</h2>
A user has received a phishing email and forwarded it to the SOC. Can you investigate the email and attachment to collect useful artifacts?
<br />


<h2>Languages and Commands Used</h2>

- <b>Bash Shell </b> 
- <b>ls</b>
- <b>chmod</b>

<h2>Environments Used </h2>

- <b>Linux Server</b> 

<h2>Program walk-through:</h2>

<p align="center">
Check file and directory details: <br/>
<img src="https://imgur.com/OxTW10y.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<h2>ls command (Check file and directory details)</h2>
I used the ls -l command to generate a detailed listing of all files and directories within the "projects" directory. ls -la could also be used to include hidden files and displayed permissions, ownership, and other relevant details for each item. The output showed one directory (drafts), and four other project files. The permissions were displayed as 10-character strings, representing the access levels for the user, group, and others.
<br />
<h2></h2>
<p align="center">
Change file permissions: "other" shouldn't have write access to any files <br/>
<img src="https://imgur.com/QjUghzR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br /> 
<p align="center">
Change file permissions on a hidden file: read-only permissions "group & user" for file .project_x.txt <br/>
<img src="https://imgur.com/VZ8BItO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br /> 
<h2>chmod command (Change file permissions)</h2>
First I managed file permissions within the "projects" directory to ensure security and proper authorization. I used the chmod command to modify the permissions of specific files and directories. For instance, I removed write permissions for the "other" category on the project_k.txt file. This action ensured that unauthorized users could not modify the file. <br />
<br />
Secondly, I identified .project_x.txt as a hidden file due to its name starting with a period (.). I then modified its permissions using the chmod command.
I added read permissions for the group with g=r.
I added read permissions for the user with u=r. 
Using = for both "user" and "group" categories overwrites all previous permissions and executes read permissions only.
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
