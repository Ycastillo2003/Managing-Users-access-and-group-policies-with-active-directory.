![image](https://github.com/user-attachments/assets/4ebcafe1-4002-49e1-9961-38af716d541c)

# Managing Users access and group policies with active directory.

<h1>Active Directory - Prerequisites and Installation</h1>
This lab outlines how to use various features in Active Directory to centrally manage thousands of user accounts in one place—including accounts, passwords, permissions, and more. It also covers how to manage devices at scale and control access to resources across a large environment.



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute).
- Remote Desktop.
- Microsoft Powershell.
- Powershell Generate Names and Create Users script.


<h2>Operating Systems Used </h2>

- Windows Server 2022 Datacenter: Azure Edition

- Windows 10</b> (21H2)

<h2>List of Prerequisites steps</h2>


- Preparing AD infrastructure 
- Deploying Active Directory
- Creating Users With Powershell
- Group Policy and Managing  Accounts


<h2>Installation Steps</h2>

![image](https://github.com/user-attachments/assets/15c0c796-7775-4e8c-bfe2-e7ba4037c9a1)

- Lab Infrastructure Overview .

![image](https://github.com/user-attachments/assets/c65c202c-9ea3-4e44-8517-62b7305fda6f)

- Ceployment of azure virtual machines to simulate domain controller and client.

![image](https://github.com/user-attachments/assets/58114f46-5efa-401b-a306-975f5ca806ab)

- Connecting to our Dc-1(Domian controller) and turning off private and public profile firewall.

![image](https://github.com/user-attachments/assets/155a385c-fd35-44dd-972d-5f46cceb8f40)

- Changing clients-1 dns server to allow it to join the Domain and restarting client-1 virtual machine to make the new dns setting become active.

![image](https://github.com/user-attachments/assets/72b85307-b32d-4f3a-b06f-cc263b2cc6ce)

- Pinging Dc-1(Domain controller) private ip from client-1 Virtual machine on powershell and using the ipconfig /all command to ensure clients-1 dns server has changed.

![image](https://github.com/user-attachments/assets/75c2fcd5-fe85-41eb-9eef-cd234fc3f830)    ![image](https://github.com/user-attachments/assets/f66001b0-58c0-4a02-bc63-e547673d690c)

- Installing active Domain on Dc-1(Domain controller) and promoting Dc-1(Domain controller) to promoting it to domain controller.

![image](https://github.com/user-attachments/assets/718d379b-f7ec-4757-8835-418ff2852e60)

- logging back into to Dc-1(Domain controller) as a domain user.

![image](https://github.com/user-attachments/assets/a25efc35-9fcc-4057-a1c1-fdc42bd4d398)

- Creating employees and admin organizational groups and adding a admin a user (Jane Doe).

![image](https://github.com/user-attachments/assets/81d99887-bcf2-4886-b145-f34aaadfad7d)

- Adding Domain user (Jane Doe) to the domain admins security group

![image](https://github.com/user-attachments/assets/c7dfcce6-27a1-4f57-a5f1-9a27c9589249)

- Adding client-1 to my domain.

![image](https://github.com/user-attachments/assets/2fa4f754-b807-4c86-b5e6-bc9c5218481c)

- Logging back in to client-1 as Jane_doe.

![image](https://github.com/user-attachments/assets/8c0cf078-50f2-4424-888c-09752567f883)

- Giving domain users remote desktop access to this Client-1.

![image](https://github.com/user-attachments/assets/e74c9449-8705-4432-908d-860787b84c89)

- Using Powershell script to generate users for our domain.

![image](https://github.com/user-attachments/assets/c8a8faa0-9505-405a-b9d9-d153e1fd919c)

- Logging into client-1 as one of our randomly generated users.


![image](https://github.com/user-attachments/assets/a2619e23-b0be-4ac2-93fa-961c58654759)

- Configuring an account lockout poilicy for our domain.

![image](https://github.com/user-attachments/assets/f3dbc39f-86bc-4dda-a7b2-b302d6fc0d5e)

- Forcing the computer policy update to happen immidiately.


![image](https://github.com/user-attachments/assets/c0f82ac7-f05d-4ddb-95d3-8f9c98264557)    ![image](https://github.com/user-attachments/assets/65c4ce5a-8a54-4d2f-89f8-08e567b22669)

- Verifyng that my lock out poilicy has taken effect and unlocking the account for the user as well.


![image](https://github.com/user-attachments/assets/b6494099-fa8a-4ca7-a8f2-e76e69a8ac1a)

- Logging into the account and verifying that the account has been unlocked.


![image](https://github.com/user-attachments/assets/42b4e3ac-740d-427d-8ec0-37e2300c5609)

- Scannings logs as an admin to see user logon activity.
