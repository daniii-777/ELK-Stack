## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

![](Diagrams/Elk_Diagram.png)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the yml file may be used to install only certain pieces of it, such as Filebeat.

  - _TODO: Enter the playbook file._

This document contains the following details:
- Description of the Topologu
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly available, in addition to restricting access to the network.
- _TODO: What aspect of security do load balancers protect? What is the advantage of a jump box?
-Load balancers distribute incoming network traffic to the appropiate server. Load balancers assist with reducing response time, and makes the overall 
browsing experience smoother for the user. On the other hand, a jump box serves as a bridge between two trusted networks; and acting as the only point of entry 
to the network; it ensures controlled access either through SSH or RDP.  

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the data and system logs.
- _TODO: What does Filebeat watch for?
- Filebeat is resposible for monitoring, gathering, and displaying log data. 
- _TODO: What does Metricbeat record?_
- Metricbeat assists in monitoring, and providing the metrics of the systems and services that the server is hosting.

The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.

| Name     | Function | IP Address   | Operating System |
|----------|----------|--------------|------------------|
|Jump-Box-
Provisioner| Gateway  | 20.222.0.241 | Linux            |
|Web1 Japan| webserver|52.140.192.229| Linux            |
|Web2 Japan| webserver|52.140.192.229| Linux            |
|ELK-SERVER| kibana   | 20.89.250.91 | Linux            |
|Red-TeamLB| LB       |52.140.192.229| DVWA             |
### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the Jump-Box machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- _TODO: 20.222.0.241
         10.0.0.1
Machines within the network can only be accessed by SSH.
- _TODO: Which machine did you allow to access your ELK VM? What was its IP address?_
- I allowed the Jump-Box-Provisioner to have access to my ELK VM - 10.0.0.1
A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box |       Yes           |      10.0.0.1        |
|ELK-SERVER|       Yes           |    40.74.90.236      |
|   DVWA   |       No            |      10.0.0.5        |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- _TODO: What is the main advantage of automating configuration with Ansible?_
-Automating configurations through ansible allows 
The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- ...
- ...

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

![TODO: Update the path with the name of your screenshot of docker ps output](Images/docker_ps_output.png)

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- _TODO: Web1-Japan: 52.140.192.229
         Web2-Japan: 52.140.192.229

We have installed the following Beats on these machines:
- _TODO: Filebeat
         Metricbeat

These Beats allow us to collect the following information from each machine:
- _TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., `Winlogbeat` collects Windows logs, which we use to track user logon events, etc._
- -Both beats are described as lightweight shippers, and while their functions differ, they are both imperative for the delivery and supervision of log files. Filebeat is constantly either retrieving log files, scanning the location of such logs, or shipping them out. So while filebeat is in charge of centralizing 
the data, metricbeat focuses on the statistics surrounding the system and services running. 


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
