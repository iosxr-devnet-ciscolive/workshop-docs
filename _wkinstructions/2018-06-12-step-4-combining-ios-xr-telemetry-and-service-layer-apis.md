---
published: true
date: '2018-06-12 10:13 -0400'
title: 'Step 4:  Combining IOS-XR Telemetry and Service Layer APIs'
author: Akshat Sharma
tags:
  - iosxr
  - cisco
  - CLUS2018
  - devnet
  - programmability
---

{% include toc %}

## To Know More


### Service Layer APIs

These are APIs at the network infrastructure layer of the IOS-XR stack. These APIs enable model-driven access over gRPC to functionality verticals such as RIB , Label Switch Database, Interface Events and BFD events with more functionalities coming in the future.

Several key attributes of these APIs:
*  **Performance:** Highly Performant API enabling route programming at a rate of 20000-30000 routes/second
*  **Model Driven:** Protobuf IDL based model for RPC and data structure definitions
*  **Multi-Language Client support:** Choose any language binding supported by gRPC to write a service-layer API client

To learn more, head over to:

><https://xrdocs.io/cisco-service-layer/>

### Streaming Telemetry

Streaming Telemetry helps deliver a push-based technique for getting operational data out of an IOS-XR box - using model-driven YANG paths with the capacity to integrate with a wide variety of open source tools like pipeline, kafka, influxdb, ELK, prometheus and more or just write a gRPC telemetry client of your own and subscribe to the stream

Key features:

*  **Model Driven:** Structured data is sent back to collectors/clients allowing easy parsing and integration with larger remediation/alarm systems.
*  **Highly Scalable and Performant:** Telemetry has been shown to beat SNMP both at scale and at the rate at which data can be streamed out without negligible effect on the resources of the network device.
*  **Wide variety of integrations:** Open Source tools and integrations available for a vast set of monitoring tools in the industry.

To learn more, head over to:

><https://xrdocs.io/telemetry/>


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


The topology we will be dealing with looks something like this:

![topology.png]({{site.baseurl}}/images/topology.png)


Ask the proctor for your credentials to access the pod. Click on the "VNC" option under Devnet_Pods/Podx where Podx is the pod assigned to you.
{: .notice--warning}


## Open up Sublime to view the code pieces we will be dealing with
![sublime.png]({{site.baseurl}}/images/sublime.png)

Keep this open to view the code at any point. Drop back into the terminal to continue.

