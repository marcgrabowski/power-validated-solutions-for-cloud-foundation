# Release History

## v1.4.0 (2022-22-02)
- Enhanced all Developer Ready Infrastructure Solution cmdlets for better error handling and message output.
- Added `Undo-NetworkSegment` cmdlet to remove an NSX segment from an NSX Management Cluster.
- Added `Undo-PrefixList` cmdlet to remove an NSX Prefix List from an NSX Management Cluster.
- Added `Undo-RouteMap` cmdlet to remove an NSX Route Map from an NSX Management Cluster.
- Added `Undo-DatastoreTag` cmdlet to remove the vSphere Tag and Category from a datastore in vCenter Server.
- Added `Undo-StoragePolicy` cmdlet to remove a VM vSphere Storage Policy from vCenter Server.
- Added `Undo-Registry` cmdlet to disable the Embedded Harbor Registry on the Supervisor Cluster.
- Added `Undo-SupervisorCluster` cmdlet to remove the Supervisor Cluster.
- Added `Undo-ContentLibrary` cmdlet to remove a Content Library from the Workload Domain vCenter Server.
- Added `Undo-Namespace` cmdlet to remove a Namespace from the Supervisor Cluster.
- Added `Undo-NamespacePermission` cmdlet to remove permissions from a Namespace.
- Added `Undo-TanzuKubernetesCluster` cmdlet to remove a Tanzu Kubernetes Cluster from the Supervisor Cluster.
- Added `Add-NsxtNodeProfileSyslogExporter` cmdlet to add a syslog exporter to the default node profile or specified node profile id.
- Added `Undo-NsxtNodeProfileSyslogExporter` cmdlet to remove all syslog exporter from the default node profile or specified node profile id.

## v1.3.0 (2022-25-01)
- Fixed `New-vRSLCMLockerLicense` cmdlet where depending on the speed of the system the license would be added but POST_VALIDATION would fail.
- Enhanced all Identity and Access Management Solution cmdlets for better error handling and message output.
- Enhanced all vRealize Operations Manager cmdlets for better error handling and message output.
- Enhanced all vRealize Log Insight cmdlets for better error handling and message output.
- Enhanced all vRealize Automation cmdlets for better error handling and message output.
- Enhanced `Set-vCenterPermission` cmdlet to set permissions on non-nested folders.
- Enhanced `Enable-SupervisorCluster` cmdlet with better pre-validation.
- Renamed `Add-NsxtVidmGroupRole` cmdlet to `Add-NsxtVidmRole`, to add support for assigning both users and groups roles in NSX-T Data Center.
- Added `Add-ResourcePool` cmdlet to create a resource pool in the Workload Domain specified.
- Added `Undo-ResourcePool` cmdlet to remove a resource pool based on the Workload Domain specified.
- Added `Update-vRAOrganizationDisplayName` cmdlet to configure the Organization Display Name in vRealize Automation.
- Added `Add-vROPSAdapterPing` cmdlet to add a Ping Adapter to vRealize Operations Manager.
- Added `Enable-vROPSManagementPack` cmdlet to upload and install the SDDC Health Management Pack to vRealize Operations Manager.
- Added `Update-vROPSAdapterSddcHealth` cmdlet to rename the SDDC Health Adapters in vRealize Operations Manager.
- Added `Add-vROPSAdapterSddcHealth` cmdlet to add SDDC Health Adapters for the Remote Collectors in vRealize Operations Manager.
- Added `Add-vROPSAlertPluginEmail` cmdlet to add an Email Alert Plugin to vRealize Operations Manager.
- Added `Register-vROPSManagementPack` cmdlet to activate / deactivate Native Management Packs in vRealize Operations Manager.
- Added `Import-vROPSUserGroup` cmdlet to import a user group and assign access in vRealize Operations Manager.
- Added `Add-vROvCenterServer` cmdlet to add a workload domain vCenter Server instance to the embedded vRealize Orchestrator.
- Added `Remove-vROvCenterServer` cmdlet to remove a workload domain vCenter Server instance from the embedded vRealize Orchestrator.
- Added `Add-vROTrustedCertificate` cmdlet to import a trusted certificate to the embedded vRealize Orchestrator using a PEM-encoded file.
- Added `Import-vROPSNotification` cmdlet to import notifications using comma separated value file to vRealize Operations Manager.
- Added `Add-vRANotification` cmdlet to configure the smtp notification settings in vRealize Automation.
- Added `New-vRACloudAccount` cmdlet to add Cloud Accounts for a Workload Domains vCenter Server and NSX Management Cluster in vRealize Automation.
- Added `Undo-vRACloudAccount` cmdlet to remove the Cloud Accounts for a Workload Domains vCenter Server and NSX Management Cluster in vRealize Automation.
- Added `Update-vRACloudAccountZone` cmdlet to update the configuration of the Cloud Account Zone for a Workload Domain in vRealize Automation.
- Added `Add-vRAUser` cmdlet to add an organization role and a service role to a user account in vRealize Automation.
- Added `Undo-vRAUser` cmdlet to remove an organization role and all service roles from a user account in vRealize Automation.
- Added `Add-vRAGroup` cmdlet to add an organization role and a service role to a group in vRealize Automation.
- Added `Undo-vRAGroup` cmdlet to remove an organization role and all service roles from a group account in vRealize Automation.
- Added `Undo-IdentitySource` cmdlet to remove an Identity Provider from vCenter Server.
- Added `Undo-SddcManagerRole` cmdlet to remove access for a user in SDDC Manager.
- Added `Add-SsoUser` cmdlet to add a Single Sign-On domain user.
- Added `New-vRSLCMDatacenter` cmdlet to add a datacenter in vRealize Suite Lifecycle Manager.
- Added `Undo-vRSLCMDatacenter` cmdlet to remove a datacenter from vRealize Suite Lifecycle Manager.
- Added `New-vRSLCMDatacenterVcenter` cmdlet to add a vCenter Server to a datacenter in vRealize Lifecycle Manager.
- Added `Export-WSAJsonSpec` cmdlet to generate the deployment JSON for Clustered Workspace ONE Access.
- Added `New-WSADeployment` cmdlet to trigger the deployment of Clustered Workspace ONE Access via vRealize Suite Lifecycle Manager.
- Added `Add-WorkspaceOneDirectoryConnector` cmdlet to add a connector to the Identity Provider in Workspace ONE Access.
- Added `Add-vRLIAlertDatacenter` cmdlet to create vRealize Log Insight alerts by datacenter.
- Added `Add-vRLIAlertVirtualMachine` cmdlet to create vRealize Log Insight alerts by virtual machine.
- Added `Undo-vRLIAlert` cmdlet to remove alerts from vRealize Log Insight.
- Added Sample Notification Templates in the SampleNotifications folder:
    - `vrli-vcf-datacenter.json` defines the vRealize Log Insight alerts that should be configured for VMware Cloud Foundation at the datacenter level.
    - `vrli-vcf-vmVrslcm.json` defines the vRealize Log Insight alerts that should be configured for vRealize Suite Lifecycle Manager.
- Added Sample Scripts in the SampleScripts\iom folder, each script uses the Planning and Preparation Workbook as the input source:
    - `iomDeployVrealizeOperations.ps1` automates the install and config of vRealize Operations for Intelligent Operations Management for VMware Cloud Foundation.
    - `iomConfigureVrealizeOperations.ps1` automates the integration config of vRealize Operations for Intelligent Operations Management for VMware Cloud Foundation.

## v1.2.0 (2021-30-11)
- Fixed `Add-GlobalPermission` where an error is thrown when Internet Explorer has not been launched in the operating system.
- Fixed `Set-DatastoreTag` where it was failing to create a single tag and category when multiple vCenter Servers in the Single-Sign On domain.
- Fixed `Add-StoragePolicy` where is was failing to add the storage policy when multiple vCenter Servers in the Single-Sign On domain.
- Enhanced `Move-VMtoFolder` cmdlet to check the name of VM provided and skip if it does not exist.
- Enhanced `Add-WorkspaceOneDirectory` cmdlet so that it can be used with Clustered Workspace ONE Access.
- Enhanced `Set-WorkspaceOneSmtpConfig` cmdlet to skip the configuration if the SMTP Server configuration is already performed.
- Added `Export-vRLIJsonSpec` cmdlet to generate the Json specification file needed to deploy vRealize Log Insight via vRealize Lifecycle Suite Manager.
- Added `New-vRLIDeployment` cmdlet to deploy vRealize Log Insight via vRealize Lifecycle Suite Manager in VMware Cloud Foundation aware mode.
- Added `Add-vRLIAuthenticationWSA` cmdlet to support configuring Workspace ONE Access integration with vRealize Log Insight.
- Added `Add-WorkspaceOneDirectoryGroup` cmdlet to Sync additional Active Directory groups with Workspace ONE Access.
- Added `Export-vROPSJsonSpec` cmdlet to generate the Json specification file needed to deploy vRealize Operations Manager via vRealize Lifecycle Suite Manager.
- Added `New-vROPSDeployment` cmdlet to deploy vRealize Operations Manager via vRealize Lifecycle Suite Manager in VMware Cloud Foundation aware mode.
- Added `Export-vRASJsonSpec` cmdlet to generate the Json specification file needed to deploy vRealize Automation via vRealize Lifecycle Suite Manager.
- Added `New-vRADeployment` cmdlet to deploy vRealize Automation via vRealize Lifecycle Suite Manager in VMware Cloud Foundation aware mode.
- Added `Install-vRLIPhotonAgent` cmdlet to download, install and configure the vRealize Log Insight Agent on Photon Operating System.
- Added `Add-vRLIAgentGroup` cmdlet to create an Agent Group in vRealize Log Insight.
- Added `Register-vRLIWorkloadDomain` cmdlet to connect/disconnect a Workload Domain with vRealize Log Insight.
- Added `Set-vRLISyslogEdgeCluster` cmdlet to configure the Syslog settings for each NSX Edge node within a Workload Domains NSX Edge Cluster.
- Added `Add-vRLISmtpConfiguration` cmdlet to configure the SMTP Server settings for vRealize Log Insight.
- Added `Add-vRLILogArchive` cmdlet to configure Email Notifications, Retention and Archive Location for vRealize Log Insight.
- Added `Register-vROPSWorkloadDomain` cmdlet to connect/disconnect a Workload Domain with vRealize Operations Manager.
- Added `Add-vROPSCurrency` cmdlet to configure the currency for vRealize Operations Manager.
- Added `Add-vROPSGroupRemoteCollectors` cmdlet to create a Remote Collector Group and assign the remote collectors in vRealize Operations Manager.
- Added `Update-vROPSAdapterVcenter` cmdlet to update the Remote Collector Group assignment for the vCenter Server Adapter in vRealize Operations Manager.
- Added `Add-vROPSCredentialNsxt` cmdlet to create an NSX credential in vRealize Operations Manager.
- Added `Add-vROPSAdapterNsxt` cmdlet to create an NSX Adapter and Start Collection in vRealize Operations Manager.
- Added `Undo-vRSLCMLockerPassword` cmdlet to remove a password from the vRealize Suite Lifecycle Manager Locker.
- Added `Undo-vRSLCMLockerCertificate` cmdlet to remove a certificate from the vRealize Suite Lifecycle Manager Locker.
- Added `Undo-vRSLCMLockerLicense` cmdlet to remove a license from the vRealize Suite Lifecycle Manager Locker.
- Added `Undo-VMFolder` cmdlet to remove a folder from vCenter Server.
- Added `Add-vRLIAuthenticationGroup` cmdlet to assign vRealize Log Insight roles to Workspace ONE Access Groups.
- Added Sample Scripts in the SampleScripts\iam folder, each script uses the Planning and Preparation Workbook as the input source:
    - `iamConfigureVsphere.ps1` automates all the configuration of vSphere/SDDC Manager elements for Identity and Access Management for VMware Cloud Foundation.
    - `iamConfigureWorkspaceOne.ps1` automates all the configuration of Workspace ONE Access elements for Identity and Access Management for VMware Cloud Foundation.
    - `iamConfigureNsx.ps1` automates all the configuration of the NSX elements for Identity and Access Management for VMware Cloud Foundation.
- Added Sample Scripts in the SampleScripts\ila folder, each script uses the Planning and Preparation Workbook as the input source:
    - `ilaDeployVrealizeLogInsight.ps1` automates the install and config of vRealize Log Insight for Intelligent Logging and Analytics for VMware Cloud Foundation.
    - `ilaConfigureVrealizeLogInsight.ps1` automates the integration config of vRealize Log Insight for Intelligent Logging and Analytics for VMware Cloud Foundation.
- Added `New-SupervisorClusterCSR` cmdlet to create a new certificate signing request for the defined Supervisor Cluster.
- Added `Add-SupervisorClusterCertificate` cmdlet to add a signed TLS certificate for the defined Supervisor Cluster.
- Added `Add-NamespaceVmClass` cmdlet to add an existing VM Class to a Supervisor Namespace.

## v1.1.0 (2021-05-10)
- Fixed `Set-vCenterPermission` where a failure can occur if the workload domain does not follow the same naming as the vCenter Server.
- Enhanced `Add-VmStartupRule` to check both VM Groups exists before attempting to create the VM-to-VM Group.
- Enhanced `Add-ContentLibrary` to support creation of both Published and Subscription Content Libraries.
- Added `New-vRSLCMLockerPassword` cmdlet to support adding passwords to the vRealize Lifecycle Suite Manager Locker.
- Added `New-vRSLCMLockerLicense` cmdlet to support adding licenses to the vRealize Lifecycle Suite Manager Locker.
- Added `Add-VmGroup` cmdlet to support adding Virtual Machines to existing VM Groups (availability Zones in particular).
- Added a number of new functions to support automation of the Site Protection and Disaster Recovery solution:
    - `Install-SiteRecoveryManager`
    - `Install-vSphereReplicationManager`
    - `Connect-DRSolutionTovCenter`
    - `Install-VAMICertificate`
    - `Backup-VMOvfProperties`
    - `Restore-VMOvfProperties`
    - `Copy-vRealizeLoadBalancer`

## v1.0.1 (2021-16-09)
- Fixed the way Certificate file is read in `Add-WSALdapDirectory` to avoid truncation of certificate data.
- Fixed `Add-ContentLibrary` where creation using subscription URL was failing.
- Fixed `Add-VMFolder` where it was creating a folder in each vCenter Server in the Single Sign-On Domain.

## v1.0.0 (2021-24-08)
- Initial Module Release