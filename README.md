<img src="https://www.cloudera.com/content/dam/www/marketing/media-kit/logo-assets/cloudera_logo_darkorange.png" alt="drawing" width="200"/> <img src="https://s3.amazonaws.com/hashicorp-marketing-web-assets/brand/Vagrant_VerticalLogo_FullColor.rkvQk0Hax.svg" alt="drawing" height="200"/> <img src="https://www.virtualbox.org/graphics/vbox_logo2_gradient.png" alt="drawing" height="200"/>

## Introduction

Setting up a Hadoop ecosystem for learning, developing, and testing could be a time consuming task.
[Cloudera](https://www.cloudera.org) offers a guide for installing a Proof-of-Concept version of their Hadoop platform called [HDP].
This repository aims to automate the configuration of a cluster in a local machine using [Virtualbox](https://www.virtualbox.org/) and [Vagrant](https://www.vagrantup.com/). **Note:** The guide explains how to install HDP, that is good for learning and testing, but not for production or commercial use.

The idea of repository was inspired by [ambari-vagrant](https://github.com/u39kun/ambari-vagrant). Most of the configuration is taken from there. 

## Requisites
- A computer with at least 16GB of RAM and 8 CPU threads.
- This works with Mac OS, Linux, and Windows 10.
    -   For Windows 10:
        - Execute the scripts in the Windows Subsystem for Linux (WSL)
        - Install the same version of Vagrant in Windows and WSL
        - Virtualbox must be installed only on Windows 10
        - Add the following to your .bashrc: `export VAGRANT_WSL_ENABLE_WINDOWS_ACCESS="1"`
        - Clone the repository to `C:/cdh-vagrant/` which is accessible from `/mnt/c/cdh-vagrant/` in WSL
        - For more details check [Vagrant and Windows Subsystem for Linux](https://www.vagrantup.com/docs/other/wsl.html).
- Ideally 4 VMs with 8GB of RAM and 4 cores should work fine if you want to use more than the Essentials

## Installation Guide
- Clone this repository using `git clone https://github.com/frederickayala/cdh-vagrant.git`
    - If you are using Windows the repository must be cloned to a Windows drive path (e.g., `C:/cdh-vagrant` or `/mnt/c/cdh-vagrant`
- Go to the repository folder using `cd cdh-vagrant` 
- Append the lines in `append-to-hosts-file` to your hosts files. 
    - For MacOS, Linux, and WSL the file is located in `/etc/hosts`
    - For Windows the file is located in `C:\Windows\System32\Drivers\etc\hosts` 
    - Windows user must append the lines in both WSL and Windows. 
- Check the *HARDWARE NOTE* in the Vagrantfile to verify that matched your computer capabilities.
- Run the command `bash up.sh 3` this will start three VMs.
    - You can add up to 8 hosts. 
- If it is the first time that you are running vagrant run `vagrant init`
- SSH to the node `vagrant ssh c7401` the password is `vagrant`
- Switch to sudo using `sudo su -`
- Download Ambari using `wget -nv http://public-repo-1.hortonworks.com/ambari/centos7/2.x/updates/2.7.3.0/ambari.repo -O /etc/yum.repos.d/ambari.repo`
- Install Ambari server: `yum install ambari-server`
- Setup ambari server: `ambari-server setup`
- Start the service: `ambari-server start`
- To check the status of the service: `ambari-server status`
- Set port forwarding 8080

## Practical notes
- Hive agent install error:
1) wget https://dev.mysql.com/get/Downloads/Connector-J/mysql-connector-java-5.1.48.tar.gz
2) tar -xvzf mysql-connector-java-5.1.48.tar.gz
3) cd mysql-connector-java-5.1.48
4) cp mysql-connector-java-5.1.48.jar /var/lib/ambari-server/resources/mysql-connector-java.jar

## Cluster Ops
- SSH to a node: `vagrant ssh`
- Suspend the cluster: `vagrant suspend`
- Resume the cluster: `vagrant resume`
- To erase all the VMs: `vagrant destroy -f`
- Check the status of the VMs: `vagrant status`

## What next?
- We are will add exercises for the most common tools. Coming soon!
