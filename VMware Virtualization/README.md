<h1>VMware Workstation Pro Virtualization Lab</h1>
</br>
<h2>Skills Demonstrated</h2>  

- VMware Workstation Pro installation
- VMs creation and hardware configuration
- Snapshot creation and recovery
- VM cloning

<h2>Installation</h2>  

- Downloaded VMware Workstation Pro from Broadcom.
- Installed using the default configuration.
- Verified hardware virtualization (Intel VT-x/AMD-V) was enabled.
- Confirmed VMware launched successfully.

<h2>VMs creation and hardware configuration</h2>  

<h4>Configuration:</h4>  

| Guest OS | Windows 11 Enterprise Evaluation | Windows Server 2022 Evaluation |
|---------|------------|---------------------|
| CPUs | 4 | 4 |
| Memory | 6GB | 8GB |
| Disk | 50GB | 60GB |
| Network | Bridged | Bridged |

<h4>Steps:</h4>  

- Clicked 'Create a New Virtual Machine'
- Chose 'Typical' configuration
- Selected ISO
- Created Virtual Disk stored as a single file
- Allocated CPUs and Memory
- Configured network adapter to use Bridged to allow VMs communicate with each other and host
- Finished wizard and powered on VMs
- Installed VMware Tools

<h3>Problems encountered</h3>
<h4>1. Windows Server 2022 Evaluation asked for licence key</h4>
<h4>Solution</h4>  

- Chose 'I will install operating system later'
- Finished wizard and added ISO to Virtual CD/DVD Drive
- Powered on VM and confirmed that it works
<h4>2. VMs were not able to ping each other</h4>
<h4>Solution</h4>  

- Enabled firewall inbound rule "File and Printer Sharing (Echo Request - ICMPv4-In)"

<h3>Results</h3>  

Both VMs booted correctly and were able to ping each other.

<img width="1257" height="996" alt="Screenshot from 2026-08-08 18-16-19" src="https://github.com/user-attachments/assets/651d17a7-23a2-4513-98df-41f18dcd2fd4" />
<img width="1163" height="996" alt="Screenshot from 2026-08-08 18-16-31" src="https://github.com/user-attachments/assets/59a2ca79-815a-4c59-8679-22529808880e" />

<h2>Snapshot Creation and Recovery</h2>  

<h3>Snapshot Creation</h3>
<h4>Steps performed</h4>  

- Opened VM > Snapshot > Take Snapshot
- Named snapshot and described it

<img width="1034" height="895" alt="Screenshot from 2026-08-08 18-26-44" src="https://github.com/user-attachments/assets/f5f4bb92-a2c6-47ce-9d30-6c8d597a3a75" />

<h4>Created text file to test snapshot recovery.</h4>  

<img width="1162" height="992" alt="Screenshot from 2026-08-08 18-33-50" src="https://github.com/user-attachments/assets/f181c324-468d-49e7-8f81-c31dc54a4677" />

<h3>Snapshot Recovery</h3>

<h4>Steps performed</h4>  

- Opened VM > Snapshot > Snapshot Manager
- Selected snapshot created before changes
- Clicked Go To to start recovery

<h4>Verification</h4>  

Snapshot recovered successfully.  

<img width="1169" height="1000" alt="Screenshot from 2026-08-08 18-39-26" src="https://github.com/user-attachments/assets/235d9c5f-3726-49b2-a8d2-18664cee4917" />

<h2>VM Cloning</h2>

<h3>Steps performed</h3>  

- Right-clicked VM tab and selected Manage > Clone
- Selected Full Clone and finished wizard
- Started cloned VM

<h3>Verifiaction</h3>  

Cloned VM started and worked normally.

<img width="1166" height="994" alt="Screenshot from 2026-08-08 18-46-08" src="https://github.com/user-attachments/assets/ba162cae-e74f-41c8-9535-4c20e5028a2f" />
