## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

![](Diagrams/diagram.png)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the config or yml files may be used to install only certain pieces of it, such as Filebeat.

  - [Ansible Config](https://github.com/AnthonyMaret/project13/blob/main/Ansible/ansible.cfg)
  - [Filebeat Config](https://github.com/AnthonyMaret/project13/blob/main/Ansible/filebeat-config.yml)
  - [Filebeat Playbook](https://github.com/AnthonyMaret/project13/blob/main/Ansible/filebeat-playbook.yml)
  - [Metricbeat Config](https://github.com/AnthonyMaret/project13/blob/main/Ansible/metricbeat-config.yml)
  - [Metricbeat Playbook](https://github.com/AnthonyMaret/project13/blob/main/Ansible/metricbeat-playbook.yml)

This document contains the following details:
- Description of the Topology
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly available, in addition to restricting unauthorized connections to the network.
- What aspect of security do load balancers protect? What is the advantage of a jump box?
-  Answer:

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the _____ and system _____.
- What does Filebeat watch for?
-  Answer:

- What does Metricbeat record?
-  Answer:

The configuration details of each machine may be found below.

| Name    | Function           |              IP Address                  |  OS   |
|---------|--------------------|------------------------------------------|-------|
| jumpbox | Gateway            | Public: 20.127.15.15  Private: 10.0.0.4  | Linux |
| web-1   | Web Server         | Public: 20.25.13.5    Private: 10.0.0.5  | Linux |
| web-2   | Web Server         | Public: 20.25.13.5    Private: 10.0.0.6  | Linux |
| elk     | ELK Server         | Public: 20.122.99.157 Private: 10.1.0.4  | Linux |

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the _____ machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- _TODO: Add whitelisted IP addresses_

Machines within the network can only be accessed by _____.
- _TODO: Which machine did you allow to access your ELK VM? What was its IP address?_

A summary of the access policies in place can be found in the table below.

| Name          | Publicly Accessible | Allowed IP Addresses |
|---------------|---------------------|----------------------|
| Jumpbox       | Yes                 | 98.31.39.159         |
| web-1         | No                  |                      |
| web-2         | No                  |                      |
| elk           | Yes                 | 98.31.39.159         |
### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- _TODO: What is the main advantage of automating configuration with Ansible?_

The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- ...
- ...

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.
![](Progress-Screenshots/elk-container-created.png)

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- List the IP addresses of the machines you are monitoring.
-  Answer: web-1: 10.0.0.5 web-2: 10.0.0.6

We have installed the following Beats on these machines:
- Specify which Beats you successfully installed.
-  Answer: Filebeat and Metricbeat

These Beats allow us to collect the following information from each machine:
- _TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., `Winlogbeat` collects Windows logs, which we use to track user logon events, etc._

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the _____ file to _____.
- Update the _____ file to include...
- Run the playbook, and navigate to ____ to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it?_
- _Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on?_
- _Which URL do you navigate to in order to check that the ELK server is running?

_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._

