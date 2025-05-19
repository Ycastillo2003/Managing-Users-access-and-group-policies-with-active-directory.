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

