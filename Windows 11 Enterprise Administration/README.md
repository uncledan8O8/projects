<h1>Windows 11 Enterprise Administration Lab</h1>
</br>
<h2>Objective</h2>
Gain hands-on experience administrating Windows 11 Enterprise by completing common tasks.
<h2>Skills Demonstrated</h2>  

- Local user management
- Windows Security
- Windows Update
- Software installation
- BitLocker
- File sharing
- Remote Desktop
- Disk Management
- Device Manager
- Event Viewer
- Performance Monitoring
- Troubleshooting

<h2>User Administration</h2>

<h3>Objective</h3>
Create different user accounts and assign permissions.
<h4>Steps performed</h4>  

- Opened Computer Management
- Navigated to Users and Groups
- Created Standard User
- Created Administrator User
- Added Administrator user to Administrators group
- Tested login
<img width="983" height="705" alt="Screenshot 2026-07-15 195827" src="https://github.com/user-attachments/assets/0e4a4b25-be39-406f-8b1b-4d9eb2db1332" />

<h2>Windows Security</h2>  

<h3>Objective</h3>  
Review the Windows Security to ensure system is protected.

<h3>Virus & Threat Protection</h3>

- Confirmed that Microsoft Defender was enabled
- Performed Quick Scan
- Verified that no threats were found

<h3>Firewall & Network Protection</h3>  

- Confirmed that firewall is turned on
- Added inbound rule for port 22/tcp

<h3>App & Browser Control</h3>  

- Confirmed that SmartScreen and Smart App Control is enabled to help protect system against malicious websites and applications

<h3>Device Security</h3>  

- Reviewed Device Security and confirmed that system did not report any issues 

<h3>Results</h3>

No threats were found and all major system protections were enabled.
</br>

<img width="1201" height="931" alt="Screenshot 2026-07-16 191231" src="https://github.com/user-attachments/assets/4e139189-ad33-4ef1-89a0-3f606288f1e9" />  

<h2>Windows Update</h2>
<h3>Objective</h3>
Ensure all security and other updates are installed

<h4>Steps performed</h4>  

- Checked for updates
- Installed all available updates
- Verified that system function correctly
<img width="1197" height="933" alt="Screenshot 2026-07-16 191908" src="https://github.com/user-attachments/assets/7f28c7e3-3ce1-4dfb-a665-78b47a8d87c2" />

<h2>Software Installation</h2>
<h3>Applications installed:</h3>  

- Brave Browser
- VMware Workstation Pro
- WinRAR

Verified that all applications function correctly  
</br>
<img width="1502" height="1046" alt="Screenshot 2026-07-16 192907" src="https://github.com/user-attachments/assets/6acc6cd5-4f6f-4640-b797-69b2a1e762d3" />

<h2>BitLocker</h2>
<h3>Objective</h3>  
Enable BitLocker Drive Encryption to prevent unauthorised access to operating system.

<h4>Steps performed</h4>

- Opened BitLocker Drive Encryption control panel
- Selected C: Driver and clicked "Turn BitLocker on"
- Saved recovery key to secure location
- Selected "Encrypt entire drive"
- Chose "Compatible Mode"
- Started encryption process
- Verified that drive C:\ is encrypted

<h3>Results</h3>  

BitLocker is enabled successfully. Operating system is now encrypted.

</br>
<img width="1121" height="868" alt="Screenshot 2026-07-24 161259" src="https://github.com/user-attachments/assets/b3144386-0f91-4537-a78b-20b89b119686" />

<h2>File Sharing</h2>
<h3>Objective</h3>
Create shared folder on Windows 11 and manage access using share permissions.

<h4>Steps performed</h4>

- Created folder named TEST in C:\ drive
- Enabled file sharing for this folder
- Mapped drive on other system
- Configured share permissions: Administrators: Full, Standard Users: Read
- Verified that shared folder is accessible from other system on network
- Verified that administrators have full control and standard users have read only permission
</br>

Share Permissions  
<img width="717" height="443" alt="Screenshot 2026-07-24 173119" src="https://github.com/user-attachments/assets/4fb6d8ae-6bf9-4831-803e-427f89384058" />  

</br>

Folder accessed from other system on network  
<img width="1023" height="589" alt="Screenshot 2026-07-24 173606" src="https://github.com/user-attachments/assets/76187116-94f0-42d2-8c0c-60c8f733854c" />

<h2>Remote Desktop</h2>

<h3>Objective</h3>
Configure Remote Desktop to allow remote administration of Windows 11.

<h4>Steps performed</h4>

- Opened: Settings > System > Remote Desktop
- Enabled Remote Desktop
-  
