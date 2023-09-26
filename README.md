# How to create a Red Hat JBoss Enterprise Application Platform (EAP) using Ansible and RHEL
This Ansible script serves as the default implementation for setting up a JBoss EAP Cluster with an Apache mod_cluster load balancer. Prior to initiating the installation procedure, ensure that all prerequisites are met. Customize this script to tailor the default configurations according to your specific needs.

## Requeriments

* Bastion Server.
* Host 1 - A Virtual Machine RHEL 9.2 for Domain Controller Server.
* Hosts 2, 3, 4 - Virtual Machines RHEL 9.2 for Workservers.
* Hosts 5 and 6 - Virtual Machines RHEL 9.2 for load balancer. 
* Ansible [core 2.14.8].
* JBoss EAP 7.4.

## Summary

## Downloading JBoss EAP 
This section outlines the steps to download JBoss EAP and apply patches for updates.

### Installer
1. The first step entails downloading the JBoss EAP server from the ([Red Hat Customer Portal](https://access.redhat.com)).
2. Save the ZIP file into the 'packages/installer' folder within your script directory.

### Paches
This step is not necessary if you do not intend to apply updates to JBoss EAP patches; however, we highly recommend updating to the latest version. For this tutorial, the current version is 7.4.12.

1. The first step entails downloading the JBoss EAP Pacthes from the ([Red Hat Customer Portal](https://access.redhat.com)).
2. Save the ZIP file into the 'packages/patches' folder within your script directory.

## Ansible Script

The Ansible script is structured into three primary folders:
.__
├── **group_vars**__
├── **packages**__
│   ├── installer__
│   └── patches__
└── **roles**__
    ├── domain-controller
    │   ├── config
    │   └── tasks
    ├── jboss-eap
    │   └── tasks
    ├── jboss-hosts
    │   ├── config
    │   └── tasks
    ├── jboss-patch-apply
    │   └── tasks
    ├── mod-cluster
    │   ├── config
    │   └── tasks
    ├── mod-cluster-registry
    │   └── tasks
    ├── subscription
    │   └── tasks
    └── update-rhel
        └── tasks

### Folder group_vars

In the "group_vars" folder, we house global environment variables. These variables are defined in the "all.yml" file, allowing you to modify default values as per your specific requirements.


## Architeture Concepts 

## Cluster EAP

## Load Balancer

## Executing script

## Related Guides

