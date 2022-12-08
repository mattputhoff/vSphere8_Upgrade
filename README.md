# vSphere 8 Upgrade
 Tips, tricks, gotchas and resources from VMware TAM's

## What's New in vSphere 8
- [VMW - The Cloud Platform Tech Zone: What's New in vSphere 8](https://core.vmware.com/resource/whats-new-vsphere-8)
- [VMW - The Cloud Platform Tech Zone: vSphere 8 - Latest Content](https://core.vmware.com/vmware-vsphere-8)
    - **Remember this -->** [VMW - The Cloud Platform Tech Zone: vSphere 8 Upgrade Activity Path](https://core.vmware.com/vsphere-8-upgrade-activity-path)
    - [VMW - The Cloud Platform Tech Zone: vSphere Configuration Profiles](https://core.vmware.com/vsphere-configuration-profiles)
- [VMW Docs - VMware vSphere 8.0 Release Notes](https://docs.vmware.com/en/VMware-vSphere/8.0/rn/vmware-vsphere-80-release-notes/index.html) 


## Preparing for Upgrade

- [VMW Product Lifecycle Matrix](https://lifecycle.vmware.com/)
- [VMW Product Interoperabilty Matrix](https://interopmatrix.vmware.com/Upgrade?productId=1)
    - 6.5 to 8.0? NOPE!
    - 6.7 to 8.0? YES!
    - 7.0 to 8.0? OF COURSE! 
    - ![Interop Check](https://github.com/mattputhoff/vSphere8_Upgrade/blob/52d159c9cf18df3b6d74587984e2cb9469ee9c61/images/v8_Interop.jpg "Interop Check")
- [VMW Ports and Protocols](https://ports.esp.vmware.com/home/vSphere) - What Ports are Needed by vSphere 8?

## Things to Think About
- Back Up
    - [VMW Docs - File-Based Backup and Restore of vCenter](https://docs.vmware.com/en/VMware-vSphere/7.0/com.vmware.vcenter.install.doc/GUID-3EAED005-B0A3-40CF-B40D-85AD247D7EA4.html)
    - [vSphere Distributed Switch](https://vdc-repo.vmware.com/vmwb-repository/dcr-public/64ee9c63-6647-46bd-8685-32b97590c294/b5861550-655c-4498-ba7e-8b24b492bf31/doc/Export-VDSwitch.html)
- 6.7 and up (see above VMW Product Interoperabilty Matrix - Upgrade)
- Deactivate vCenter HA to simplify upgrade
- Simple and refactor your SSO domain
- Other Stuff

 ## Upgrading vSphere 
 
Upgrade preparation checklist
- Finish upgrade documentation plan 
- Gather needed software and hardware ISOs 
- Test ESXi host remote access credentials  
- Set a longer maintenance window than needed  
- Have proactive GSS ticket handy  

Upgrade order list

*An actual execution order should be in your upgrade documentation plan. The below is an example (which is not meant to be comprehensive):*

- Backup the environment  
- Upgrade vCenter server  
- Install vCenter Plugins  
- Upgrade ESXi Hosts  
- Upgrade the vSphere Distributed Switches  
- Upgrade VMware Tools  
- Upgrade VMware Virtual Hardware   

 ## What's Next

Other Stuff
- [VMW vSphere Blog - New Release Model for vSphere 8](https://blogs.vmware.com/vsphere/2022/10/new-release-model-for-vsphere-8.html)
- [vCenter build numbers and release dates (KB 2143838)](https://kb.vmware.com/s/article/2143838)  
- [ESXi build numbers and release dates (KB 2143832)](https://kb.vmware.com/s/article/2143832)
- [Is there an API?](https://developer.vmware.com/apis)
- [Scalabiltiy/Configuration Max](https://configmax.vmware.com/)

- [Upgrade from 6.7 to 7.0U3](https://github.com/arielsanchezmora/vSphere-67-Upgrade-to-7u3)
    - Special Shout to my fellow VMW TAM and great friend [Ariel Sanchez Mora](https://github.com/arielsanchezmora)
