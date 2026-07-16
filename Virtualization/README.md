<h1>VMware Workstation Pro Virtualization</h1>
</br>
<h2>Objectives</h2>  

- Install VMware Workstation Pro
- VMs creation and hardware configuration
- Snapshot creation and recovery
- VM cloning
- Basic virtual networking
- VM portability and backup

<h2>Installation</h2>  

- Downloaded VMware Workstation Pro from Broadcom.
- Installed using the default configuration.
- Verified hardware virtualization (Intel VT-x/AMD-V) was enabled.
- Confirmed VMware launched successfully.

<h2>VM Creation</h2>  

<h4>Configuration:</h4>  

| Guest OS | Windows 11 Enterprise Evaluation | Windows Server 2022 Evaluation | Ubuntu Server 26.04 LTS |
|---------|------------|---------------------|-------------------------|
| CPUs | 4 | 4 | 4 |
| Memory | 6GB | 8GB | 8GB |
| Disk | 50GB | 60GB | 40GB |
| Network | Bridged | Bridged | Bridged |

<h4>Steps:</h4>  

- Clicked 'Create a New Virtual Machine'
- Chose 'Typical' configuration
- Selected ISO
- Created Virtual Disk stored as a single file
- Allocated CPUs and Memory
- Configured network adapter to use Bridged
- Finished wizard and powered on VMs
- Installed VMware Tools

<h4>Results:</h4>  

- Windows 11 Enterprise Evaluation worked

<h3>Problems encountered</h3>
<h4>1. Windows Server 2022 Evaluation asked for licence key</h4>
<h4>Solution</h4>  

- Chose 'I will install operating system later'
- Finished wizard and added ISO to Virtual CD/DVD Drive
- Powered on VM and confirmed that it works
<h4>2. VMs were not able to ping each other</h4>
<h4>Solution</h4>  

- Enabled firewall inbound rule "File and Printer Sharing (Echo Request - ICMPv4-In)"


