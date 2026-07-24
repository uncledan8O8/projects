<h1>Active Directory</h1>  
</br>
<h2>Objective</h2>
Learn and demonstrate basic Active Directory administration tasks using Windows Server 2022.

<h2>Skills Demonstrated</h2>  

- Windows Server 2022 installation
- Domain Services configuration
- Joining a system to domain
- Creating Organizational Units (OUs)
- Creating User Accounts
- Creating Security Groups
- Resetting passwords
- Unlocking User Accounts
- Moving users between OUs
- Basic Group Policy configuration

<h2>Windows Server 2022 installation</h2>  

<h3>Objective</h3>  
Install Windows Server 2022 on VMware Workstation Pro to use as domain controller.

<h3>Installation process</h3>  

- Downloaded Windows Server 2022 Evaluation ISO
- Booted VM from ISO
- Chose Windows Server 2022 Standard Evaluation (Desktop Experience)
- Created new partition using entire virtual disk
- Installed server
- Verified that server is running correctly
- Installed all available updates
- Configured static IP
- Renamed server to DC

<h2>Active Directory Domain Services installation</h2>

<h3>Objective</h3>
Install and configure Active Directory Domain Services on Windows Server 2022 and promote the server to domain controller.  

<h3>Installation process</h3>

- Opened Server Manager
- Select "Add roles and features"
- Chose "Role-based or feature-based installation"
- Chose local server
- Selected Active Directory Domain Services
- Completed installation wizard

<h3>Promote server to domain controller</h3>  

- Opened Server Manager
- Clicked Notification flag
- Selected "Promote this server to a domain controller"
- Selected "Add a new forest"
- Named domain
- Selected Domain function level: Windows Server 2016
- Selected Domain function level: Windows Server 2016
- Enabled DNS Server
- Created DSRM password
- Completed installation wizard

<h3>Results</h3>  

Active Directory Domain Services and DNS Server installed successfully

<img width="1151" height="820" alt="Screenshot 2026-07-24 202654" src="https://github.com/user-attachments/assets/92d1649e-77f1-4adf-8621-a443f3c78615" /> 

<h2>Organization Units and Security Groups</h2>  

<h3>Objective</h3>
Create OUs to easily apply rules to different groups.  

<h3>Structure</h3>  

domain.local/Company:  

Departments:  

- IT
- HR
- Sales

Groups:
- IT
- HR
- Sales

Computers  

<img width="749" height="526" alt="Screenshot 2026-07-24 211157" src="https://github.com/user-attachments/assets/7978eebe-e537-4a30-a293-29c821f9bd60" />

<h2>Create Users</h2>  

<h3>Objective</h3>  
Create users and add them to Security Groups.  

<h3>Structure</h3>  

Departments:  

IT:  
- John Smith

HR:  
- Peter Parker

Sales:  
- Karen Jones
- Will Smith

<h4>Added users to Security Groups</h4>  
<img width="751" height="503" alt="Screenshot 2026-07-24 213133" src="https://github.com/user-attachments/assets/7eb578e4-cac9-457c-8650-a957603784aa" />

<h2>Join Windows 11 to the Domain</h2>  

<h3>Objective</h3>
Join Windows 11 machines to the Domain so users can authenticate using domain accounts.

<h3>Steps performed</h3>  

<h2>Configure DNS</h2>  
Changed Prefered DNS on Windows 11 machines  
</br>

<img width="967" height="702" alt="Screenshot 2026-07-24 214043" src="https://github.com/user-attachments/assets/1f8223c4-f553-480c-9e3e-c06f1f705abe" />
