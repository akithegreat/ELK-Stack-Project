# ELK-Stack-Project

## Cloud Network
This is a collection of Linux Scripts and Ansible Scripts from my CyberClass.
Most of the scripts are used to configure cloud servers with differnt docker containers.

The final setup was 2 servers running vulnerable DVWA containers along with a jump box and a server running an ELK stack container.


## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

![](https://github.com/akithegreat/ELK-Stack-Project/blob/main/Diagrams/Network%20Diagram.png)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the Ansible (_YAML__) file may be used to install only certain pieces of it, such as Filebeat.

[Filebeat files](https://github.com/akithegreat/ELK-Stack-Project/tree/main/Ansible)

This document contains the following details:
- Description of the Topology
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build



### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly available, in addition to restricting inbound access to the network. A load balancer plays a significant role in the security of the network by distributing traffic across multiple servers and preventing a network from becoming overloaded with requests.

*What is the advantage of a jump box?*
- A jump box can be used as a gateway to other servers while also preventing them from being exposed to the public internet.

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the network and system logs.

*What does filebeats watch for?*

- Filebeat collects log data at specified locations then forwards them for indexing.

*What does Metricbeat record?*

- Metricbeat collects metrics from the OS such as cpu and memory and sends the statistical data to the specified location.

The configuration details of each machine may be found below.

| Name     | Function   | IP Address | Operating System |
|----------|------------|------------|------------------|
| Jump Box | Gateway    | 10.0.0.4   | Linux            |
| Elk      | Log Server | 10.1.0.4   | Linux            |
| Web 1    | Webserver  | 10.0.0.5   | Linux            |
| Web 2    | Webserver  | 10.0.0.6   | Linux            |

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the jumpbox machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:

- Home Ip Address


Machines within the network can only be accessed by each other.

*Which machine did you allow to access your ELK VM?*

- Jump-Box-Provisioner

*What was its IP address?*

- 10.0.0.4

A summary of the access policies in place can be found in the table below.

| Name       | Publicly  Accessible | Allowed IP Addresses |
|------------|----------------------|----------------------|
| Jump-Box   | No                   | Public Home IP       |
| Elk Server | NO                   | 10.0.0.4             |
| Web-1      | NO                   | 10.0.0.4             |
| Web-2      | NO                   | 10.0.0.4             |
| Web-3      | NO                   | 10.0.0.4             |
