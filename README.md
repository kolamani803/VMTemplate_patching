# ansible-vsphere-update-templates

Notes:
Tower:
ERPM getansible credentcials need to add in prod ansible tower

All VCenters: 
Need to add one service account i.e svc_ansible username in all Vcenters
Rename the Previous backups folder or keep them in safe place for refference.

**ca1-vcenter1.ad.ea.com**
parent_folder: /Cloudbolt/Cloudbolt Templates/
vcenter_datacenter: CA1

**va1-vcenter1.ad.ea.com**
parent_folder: /Cloudbolt/Cloudbolt Templates/
vcenter_datacenter: VA1

**sin-vcenter2.ad.ea.com(Singapore DC)**
parent_folder: /Cloudbolt/Cloudbolt Templates/
vcenter_datacenter: Singapore DC

**sin-vcenter2.ad.ea.com(Shangai)**
Is that mandatory to use -sha after template name in Shangai cluster if yes, we need to use Static inventory here for ansible playbook to run.
parent_folder: /Cloudbolt/Cloudbolt Templates/
vcenter_datacenter: Shanghai
Template name:
cb-centos76x64-base-sha
cb-rhel7x64-base-sha
cb-ubuntu1804x64-base-sha
cb-ubuntu2004x64-base-sha
cb-win10x64-base-sha
cb-win2k19x64-base-sha



**lhr-vcenter1.ad.ea.com**
parent_folder: /Cloudbolt/Cloudbolt Templates/
vcenter_datacenter: LHR

**mad-vcenter1.ad.ea.com**


**va1-oraclevcenter2.ad.ea.com**
parent_folder: /Cloudbolt/Cloudbolt Templates/
vcenter_datacenter: VA1

**vc.dice.ad.ea.com**
parent_folder: /Cloudbolt/Cloudbolt Templates/
vcenter_datacenter: Hosted

Redhat -
Need to removed Katello from the template before pramoting as a template
Add SSH key authentication in /etc/ssh/sshd_config for both tower servers
to check existing install Katello using below cmd 
$ rpm -qa | grep katello-ca
Remove Katello using below command 
$ yum remove < abouve command output > -y
$ yum remove katello-* -y ( Need to add this before patching and after patching to remove all the Katello's)

Windows 10:
Need to install windows update module in windows 10 template using below command
Install-Module PSWindowsUpdate




