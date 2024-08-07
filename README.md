<h1>Phishing-Analysis-Challenge</h1>

<h2>Description</h2>
A user has received a phishing email and forwarded it to the SOC. Can you investigate the email and attachment to collect useful artifacts?
<br />

<h2>Environments Used </h2>

- <b>BlueTeamLabs.online</b>
- <b>whois.domaintools.com</b> 

<h2>Lab walk-through:</h2>

<p align="center">
Who is the primary recipient of the email? <br/>
<br />
<img src="https://imgur.com/Rb96HWR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<h2></h2>
<p align="center">
<br />
What is the date and time the email was sent? <br/>
<br />
<img src="https://imgur.com/NNjPPKw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<h2></h2>
<br />
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
<h2>Summary:</h2>
In this challenge, I was tasked with investigating an email and attachment to collect useful information. The findings included:<br />
 
- Primary Recipient: The email was primarily addressed to kinnar1975@yahoo.co.uk.

- Subject: The subject of the email was "Undeliverable: Website contact form submission", likely an attempt to trick the recipient into thinking it's a legitimate communication.

- Date and Time: The email was sent on 18 March 2021 at 04:14.

- Originating IP Address: The email originated from IP 103.9.171.10, which resolves to c5s2-1e-syd.hosting-services.net.au, indicating that the email may have been sent from a server hosted in Australia.

- Malicious URL: The attachment contained a malicious URL: https://35000usdperwwekpodf.blogspot.sg?p=9swg and https://35000usdperwwekpodf.blogspot.co.il?o=0hnd. Both URLs point to sites hosted on Blogger (Blogspot), indicating that the attackers used Google's blogging platform to host their phishing or malicious content.

These findings suggest that the email was a phishing attempt, designed to deceive the recipient into clicking on a link that could lead to malicious activities.  The use of legitimate services like Blogger to host malicious content is a common tactic to avoid detection.
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
