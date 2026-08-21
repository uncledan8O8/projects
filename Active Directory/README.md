<h1>Active Directory Lab</h1>  
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
- Domain User Account Management
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
- Selected Domain functional level: Windows Server 2016
- Enabled DNS Server
- Created DSRM password
- Completed installation wizard

<h3>Verification</h3>  

Active Directory Domain Services and DNS Server installed successfully.

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

<img width="751" height="527" alt="Screenshot 2026-07-24 230323" src="https://github.com/user-attachments/assets/66581684-f205-4ed4-b243-d5cf25fd2f3b" />  

<h2>Users Creation</h2>  

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

<h3>Configure DNS</h3>  

Configured Prefered DNS on Windows 11 machines to use Domain Controller's IP address.
<img width="967" height="702" alt="Screenshot 2026-07-24 214043" src="https://github.com/user-attachments/assets/1f8223c4-f553-480c-9e3e-c06f1f705abe" />  

Confirmed communication with Domain Controller. 
<img width="974" height="508" alt="Screenshot 2026-07-24 214349" src="https://github.com/user-attachments/assets/235de8c6-4dbd-4aab-852f-2cbf30794953" />

<h3>Join the Domain</h3>  

- Settings > About
- Device specifications > Domain or workgroup
- Chose "Change..."
- Selected Member of Domain and chose domain name
- Signed in with username and password
- Restarted machine

<h3>Verification</h3>  

Windows 11 joined domain successfully and all users are able to sign-in.

<img width="1146" height="860" alt="Screenshot 2026-07-24 230825" src="https://github.com/user-attachments/assets/4085348d-3ed5-4414-a060-1f64f23709e8" />

<img width="1143" height="815" alt="Screenshot 2026-07-24 231107" src="https://github.com/user-attachments/assets/1b3ea6aa-955d-4ebd-a5c5-f3987f72178b" />

<h3>Problem encountered</h3>  

<h4>Error when tried to change domain</h4>  
<img width="456" height="173" alt="Screenshot 2026-07-24 224240" src="https://github.com/user-attachments/assets/01399267-13fa-48fd-be33-1599ae1a1e9e" />

<h4>Solution</h4>
Disabled IPv6 on the client:  

- Opened Control Panel > Network and Sharing Center
- Selected Change adapter settings
- Right-clicked Ethernet
- Selected Properties
- Unchecked Internet Protocol Version 6 (TCP/IPv6)
- Opened Command Prompt as Administrator and ran:  
ipconfig /flushdns  
ipconfig /registerdns

<h2>Basic Group Policy</h2>  

<h3>Password Policy</h3>  
<h4>Steps performed</h4>  

- Opened Server Manager
- Selected Tools > Group Policy Management
- Expanded Forest > Domains > domain.local
- Right-clicked Default Domain Policy > Edit...
- Navigated to Computer Configuration > Policies > Windows Settings > Security Settings > Account Policies > Password Policy
- Configured password policy
- Ran command: gpupdate /force

<h4>Configuration</h4>

| Setting | Value |
|-------------------------|---------------|
| Password history | 24 passwords remembered |
| Maximum password age | 60 days |
| Minimum password length | 12 characters |
| Password complexity | Enabled |

<img width="785" height="562" alt="Screenshot 2026-07-27 191620" src="https://github.com/user-attachments/assets/94eb84a7-fb0c-40ea-adb4-66c4ab59a8ac" />

<h4>Verification</h4>

Password "spiderman" did not meet password length and complexity.
<img width="786" height="591" alt="Screenshot 2026-07-27 192534" src="https://github.com/user-attachments/assets/3b0f553a-0230-4367-afbc-0a7f229ef2b9" />

Password "Ilovecookies!123" meets password policy.
<img width="698" height="506" alt="Screenshot 2026-07-27 192758" src="https://github.com/user-attachments/assets/0420991e-2535-437e-90d7-19837c7e2b22" />


<h3>Account Lockout Policy</h3>  
<h4>Steps performed</h4>  

- Opened Server Manager
- Selected Tools > Group Policy Management
- Expanded Forest > Domains > domain.local
- Right-clicked Default Domain Policy > Edit...
- Navigated to Computer Configuration > Policies > Windows Settings > Security Settings > Account Policies > Account Lockout Policy
- Configured Account Lockout Policy
- Ran command: gpupdate /force

<h4>Configuration</h4>

|  Setting | Value |
|----------|-------|
| Account lockout threshold | 5 |
| Account lockout duration | 15 minutes |
| Reset account lockout counter after | 15 minutes |

<h4>Verification</h4>

Attempt to log in with wrong password 5 times results in account lockout.

<img width="1150" height="862" alt="Screenshot from 2026-08-07 15-15-58" src="https://github.com/user-attachments/assets/ecb2a19d-f3b8-45dc-8d24-99ff1010714d" />

<h3>Desktop Wallpaper</h3>  

<h4>Steps performed</h4>  

- Created folder named Wallpaper
- Created wallpaper named wallpaper in JPEG format
- Shared Wallpaper folder
- Opened Group Policy Management
- Navigated to Forest > Domains > domain.local
- Right-clicked domain and created new GPO named Wallpaper
- Navigated to User Configuration > Policies > Administrative Templates > Desktop > Desktop
- Enabled "Desktop Wallpaper" and specified Shared Folder path \\DC\Wallpaper/wallpaper.jpg
- Applied and ran command: gpupdate /force

<h4>Verification<h4>
  
Wallpaper is successfully changed.
  
<img width="1150" height="812" alt="Screenshot from 2026-08-07 16-35-50" src="https://github.com/user-attachments/assets/cad41d73-27c1-47ff-b0bf-ae91a505329d" />

<h3>Disable Control Panel</h3>  

<h4>Steps performed</h4>  

- Opened Group Policy Management
- Navigated to Forest > Domains > domain.local
- Right-clicked domain and created new GPO named Disable Control Panel
- Navigated to User Configuration > Policies > Administrative Templates > Display
- Enabled "Prohibit access to Control Panel and PC settings"
- Ran command: gpupdate /force

<h4>Verification</h4>

System displayed restriction error when attempted to open Control Panel.

<img width="1147" height="810" alt="Screenshot from 2026-08-07 16-49-03" src="https://github.com/user-attachments/assets/e38fa863-a0a7-42ae-9d6b-964109349c16" />

<h3>Map Network Drive</h3>

<h4>Steps performed</h4>  

- Created folder named HR-shared-folder and shared with HR
- Opened Group Policy Management
- Navigated to Forest > Domains > domain.local > Company > Departments
- Right-clicked HR and created new GPO named HR Shared Folder
- Navigated to User Configuration > Preferences > Windows Settings
- Right-clicked Drive Maps > New > Mapped Drive
- Configurations: Action > Create | Location > \\\DC\HR-shared-folder | Drive Letter > Use: Z
- Ran command: gpupdate /force

<h4>Verification</h4>

Drive successfully mapped for members of HR group.

<img width="778" height="585" alt="Screenshot from 2026-08-07 17-32-20" src="https://github.com/user-attachments/assets/b6afafa8-5b45-4e59-90f4-83bb39cecba3" />

<h2>Domain User Account Management</h2>

<h3>Objective</h3>
Simulate common Active Directory user account tasks performed by IT Technicians.

<h3>Password reset</h3>  

<h4>Steps performed</h4>  

- Navigated to Active Directory Users and Computers > domain.local > Company > Departments > HR
- Right-clicked user Peter PP. Parker and chose "Reset Password"
- Created new password and checked "User must change password at next logon"

<h4>Verification</h4>

Windows asked user to change password.  

<img width="1141" height="854" alt="Screenshot from 2026-08-07 18-02-25" src="https://github.com/user-attachments/assets/6f0a2024-dcfa-469d-aafe-ce1d2844bdaa" />

<h3>Unlock account</h3>  

<h4>Steps performed</h4>  

- Entered wrong password 5 times to lock account
- Navigated to Active Directory Users and Computers > domain.local > Company > Departments > HR
- Right-clicked user Peter PP. Parker and chose "Properties"
- Selected "Account" tab and checked "Unlock account" then applied

<h4>Verification</h4>

User is able sign-in successfully.

<img width="1119" height="835" alt="Screenshot from 2026-08-07 18-10-57" src="https://github.com/user-attachments/assets/a1eb94b9-dc82-43eb-8bf8-e8e6ea0bb552" />

<h3>Disable user</h3>  

<h4>Steps performed</h4>  

- Entered wrong password 5 times to lock account
- Navigated to Active Directory Users and Computers > domain.local > Company > Departments > HR
- Right-clicked user Peter PP. Parker and chose "Disable Account"

<h4>Verification</h4>  

User is not able to sign-in.

<img width="1137" height="852" alt="Screenshot from 2026-08-07 18-15-53" src="https://github.com/user-attachments/assets/5b1f55e0-3260-4932-b84d-bb478772750e" />

<h3>Move users between OUs</h3>  

<h4>Steps performed</h4>  

- Entered wrong password 5 times to lock account
- Navigated to Active Directory Users and Computers > domain.local > Company > Departments > IT
- Right-clicked user John JS. Smith and chose "Move"
- Moved user form IT to HR

<h4>Verification</h4>

User John JS. Smith is member of HR.

<img width="753" height="525" alt="Screenshot from 2026-08-07 18-18-47" src="https://github.com/user-attachments/assets/07ecfe0c-8459-466c-b5ff-abdbb0f04b81" />
