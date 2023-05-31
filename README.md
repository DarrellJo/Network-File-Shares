<p align="center">
<img src="https://i.imgur.com/5el37LK.png" alt="Traffic Examination"/>
</p>

<h1>Network File Shares and Permissions</h1>
In this tutorial, we will demonstrate the process of network file sharing and setting permissions on the domain controller. This tutorial is a continuation of our previous lab where we configured the active directory. <br />


<h2>Video Demonstration</h2>

- ### [YouTube: Network File Shares and Permissions](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)


<h2>High-Level Steps</h2>

- Create file shares with permissions
- Attempt to access files shares
- Create a Security Group, assign permssions, test access


<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/4QMrsd6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To begin, let's log in to both of the virtual machines (VMs) that we created in our previous lab on configuring active directory. In this lab, we will primarily focus on the "dc-1" VM. Once logged in, we will proceed to create four folders: "read-access," "write-access," "no-access," and a special folder, which we can name "accounting" for demonstration purposes. This step will simplify the process and ensure clarity throughout the tutorial.
</p>
<br />

<p>
<img src="https://i.imgur.com/DYccOut.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we will add the "Domain Users" group and set the appropriate permissions for each of the respective folders. For instance, in the "read-access" folder, the "Domain Users" group should only be allowed to have read access. Similarly, we will configure permissions for the "write-access" and "no-access" folders accordingly. For the time being, we can skip the configuration of permissions for the "accounting" folder..
</p>
<br />

<p>
<img src="https://i.imgur.com/o3mEhJh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After completing the permissions setup, let's navigate to our "Client-1" VM and locate the folders we created earlier. We will now review the access levels for each folder. Upon accessing the "read-access" folder, you will notice that you can only read the files within it, but not create any new files.
</p>
<br />

<p>
<img src="https://i.imgur.com/ug1qC6d.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Finally, let's return to the Active Directory in our "DC-1" VM. We will create a new group, which will serve as our security group specifically for accountants. We can then assign the appropriate permissions to this group for the relevant folders. Afterward, we will test the access again in our "Client-1" VM to ensure that the permissions are correctly applied based on the group membership.
</p>
<br />
