<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Group Policy Management</h1>
This tutorial covers how to manage Group Policy in Active Directory, focusing on creating and configuring Group Policy Objects (GPOs) to control network settings and security policies. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- Powershell

<h2>Operating Systems Used </h2>

- Windows Server 2022, at least 2vCPUs, 8GB RAM
- Windows 10 Pro (21H2), at least 2vCPUs, 8GB RAM


<h2>High-Level Steps</h2>

- Create user accounts within the domain
- Configure account lockout settings via Group Policy
- Enable and disable user accounts

<h2>Actions and Observations</h2>

Log into DC-1 and configure the Group Policy settings to enforce an account lockout after 5 failed login attempts.

<p>
<img src="https://i.imgur.com/zLLWJ1Y.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/wcnOiMn.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p>
<img src="https://i.imgur.com/6xExS8Z.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/OjHHc3K.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>

Log into client-1 using the jane_admin account to force the policy update. Once logged in, open Command Prompt and type gpupdate /force. After the update completes, sign out of the jane_admin account.

<p>
<img src="https://i.imgur.com/5juujEZ.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>

Select a random user account you created earlier and attempt to log in 6 times with an incorrect password.

<p>
<img src="https://i.imgur.com/rOzyfYy.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p>
<img src="https://i.imgur.com/J5zBjzo.png" height="20%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>

Observe that the account has been locked out in Active Directory. Then, proceed to unlock the account.

<p>
<img src="https://i.imgur.com/7freoMF.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>

Attempt to log in with the account to verify if it has been unlocked.

<p>
<img src="https://i.imgur.com/wpJcj9w.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
Reset the password, or if not required, you can simply use the same password as before.

<p>
<img src="https://i.imgur.com/IdeSpIf.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>

Enabling and disabling accounts: Disable the previously used account in Active Directory to deactivate it.

<p>
<img src="https://i.imgur.com/I3EcGZI.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p>
<img src="https://i.imgur.com/cbPr7Kp.pn" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>




