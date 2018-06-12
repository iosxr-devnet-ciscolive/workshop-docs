---
published: true
date: '2018-06-12 08:47 -0400'
title: 'Step 1: IOS-XR ZTP Bash and Python hooks'
author: Akshat Sharma
tags:
  - iosxr
  - cisco
  - devnet
  - CLUS2018
  - iosxr
  - programmability
---


{% include toc %}

## To Know More

As part of the Zero-touch provisioning infrastructure, IOS-XR provides the option to automate CLI operations in either bash or python in the IOS-XR shell environment. This enables a large variety of integrations - including native scripts and offbox integrations with tools like Ansible

Complete CLI support: 
*  Automate CLI operations such as "show commands", "config merge", "config replace"
*  Available in bash and python: Choose the scripting language you prefer and integrate with ztp, cronjobs, onbox-apps and more


>Check out:
>
>1) [IOS-XR Bash ZTP hooks](https://xrdocs.io/software-management/tutorials/2016-08-26-working-with-ztp/#ztp_helpersh)
>2) [IOS-XR Python ZTP library](https://xrdocs.io/software-management/tutorials/2016-08-26-working-with-ztp/#ztp_helpersh)


>The vagrant environment consisting of two IOS-XRv9k instances must already be running. Verify >this by opening up a terminal and running the following commands:
>
>  ```
>  cd ~/topology
>  vagrant status
>
>  ```
> You should then see something like this:
>  ```
>  cisco@pod2:~/topology$ vagrant status
>  Current machine states:
>
>  rtr1                      running (virtualbox)
>  rtr2                      running (virtualbox)
>  devbox                    running (virtualbox)
>
>   This environment represents multiple VMs. The VMs are all listed
>   above with their current state. For more information about a specific
>   VM, run `vagrant status NAME`.
>   cisco@pod2:~/topology$ 
>  ```

{: .notice--info}




 
