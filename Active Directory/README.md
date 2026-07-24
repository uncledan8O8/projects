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

<h3>Result</h3>  

Active Directory Domain Services and DNS Server installed successfully

<img width="1151" height="820" alt="Screenshot 2026-07-24 202654" src="https://github.com/user-attachments/assets/92d1649e-77f1-4adf-8621-a443f3c78615" />
