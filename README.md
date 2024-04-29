<h1>Active Directory with Splunk: Password cracking using Crowbar</h1>



<h2>Description</h2>
This project focuses on integrating Active Directory (AD) with Splunk, a powerful platform for monitoring, searching, analyzing, and visualizing machine-generated data. By integrating AD with Splunk, organizations can gain valuable insights into user authentication, access patterns, security events, and overall system health within their Active Directory environment.





<br />


<h2>Tools and Commands Used</h2>

- <b>Crowbar</b>

<h2>Environments Used </h2>

- <b>VirtualBox VM</b>
- <b>Kali Linux</b>
- <b>Windows 10</b>
- <b>Windows Server 22</b>
- <b>Ubuntu Server 22.04</b>

<h2>Project walk-through:</h2>

<p align="center">
Network Diagram: <br/>
<img src="https://imgur.com/pEdUmkX.png" height="80%" width="80%" alt="Project walk-through"/>
<br />
  
<h2>Password crack using Crowbar:</h2>

Crowbar is a brute-force attack tool used to crack passwords. In an Active Directory environment, it can be utilized to gain access to user credentials by attempting various password combinations until a correct one is found. The process typically involves providing Crowbar with a wordlist or dictionary of potential passwords, and it systematically tries each combination against user accounts within the Active Directory until successful authentication occurs, granting unauthorized access to the system. This method exploits weak or easily guessable passwords to compromise user accounts and gain unauthorized access to the network.





<br />

<p align="center">
Crowbar attack from Kali Linux: <br/>
<img src="https://imgur.com/bJR5F1T.png" height="80%" width="80%" alt="Project walk-through"/>
<br />
<br />
Event code alert on Splunk: <br/>
<img src="https://imgur.com/KHPcF6r.png" height="80%" width="80%" alt="Project walk-through"/>
<br />
<br />
Event code alert on Splunk: <br/>
<img src="https://imgur.com/8kX9qj7.png" height="80%" width="80%" alt="Project walk-through"/>
<br />
<br />
Splunk showing attacker's machine and IP address: <br/>
<img src="https://imgur.com/BKljCZr.png" height="80%" width="80%" alt="Project walk-through"/> 
<br />
<br />
Windows event 4625 description: <br/>
<img src="https://imgur.com/YpvjbUe.png" height="80%" width="80%" alt="Project walk-through"/>
  
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
