## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

 [Azure Cloud Diagram](./Images/azure_cloud_diagram.png)

These files have been tested  and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the install_elk.yml file may be used to install only certain pieces of it, such as Filebeat.

  - [install_elk.yml](./install_elk.yml)

This document contains the following details:

- Description of the Topologuy
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly available, in addition to restricting traffic to the network.
It ensures availability to the servers while it also would support in the case of a spam-bot or DDOS attack.

A jump box was configured and used to deploy containers and control the webservers externally from the bload balancer pool. This is effective as the jump box is a hardenered external point sitting in a separate zone and without hosting any data itself. A reliable control point for the web servers.  


Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the data and system logs.

Filebeat watches for specified log events by monitoring logfiles over given locations on a server. 
Metricbeat records stats and metrics from services running on an operating system which can be exported to either Logstash or Elasticsearch.

The configuration details of each machine may be found below.


| Name     | Function | IP Address | Operating System |
| -------- | -------- | ---------- | ---------------- |
| JumpBoxProvisioner | Gateway  | 40.126.237.121   | Linux (Ubuntu 18.04)            |
| Web1     | Web Server| 10.0.0.5| Linux (Ubuntu 18.04)                  |
| Web2     | Web Server| 10.0.0.6| Linux (Ubuntu 18.04                 |
| Web3     | Web Server| 10.0.0.8| Linux (Ubuntu 18.04                 |
| ELK-VM     | ELK Server| 10.1.0.4| Linux (Ubuntu 18.04                 |
| RedTeamLB     | Load Balancer| 52.187.233.146| n/a               |
### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the ELK-VM machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:

Remove Client IP (dynamic home client IP via port 5601)

Machines within the network can only be accessed by JumpBoxProvisioner/home client.

Remove Client IP (dynamic home client IP via port 5601)
JumpBoxProvisioner (40.126.237.121)


A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
| -------- | ------------------- | -------------------- |
| JumpBoxProvisioner | No             | Remove Client IP:22 (SSH)   |
| ELK-VM         |     Yes                |  Remove Client IP:5601 (TCP)                     |
| WebVM's         |     no                |   Remove Client IP:22 (SSH)                   |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because Ansible allows for fast deployment of applications accross multiple machines at once. A clear advantage of this is consistency accross all machines in the network and the time saved not having to run installations and configuration on each individually. 

### The playbook implements the following tasks:


```
  name: Configure Elk VM with Docker 
  hosts: elk
  remote_user: webadmin
  become: true
  tasks:
  ```
  Configures and identifies the remote username in this case 'webadmin'.
 ```
  name: Install docker.io
      apt:
        update_cache: yes
        force_apt_get: yes
        name: docker.io
        state: present
```
Installs docker.io to target machine
```
 name: Install python3-pip
 apt:
 force_apt_get: yes
 name: python3-pip
 state: present
```
Uses apt module to install Python3

```
- name: Use more memory
      sysctl:
        name: vm.max_map_count
        value: '262144'
        state: present
        reload: yes
```
Increases virtual memory amount

```
-  5601:5601
-  9200:9200
-  5044:5044
```
Sepcifies exposed ports


The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

[ELK_Container.png](./Images/ELK_Container.png)

### Target Machines & Beats

This ELK server is configured to monitor the following machines:

| Web1: 10.0.0.5| 
| Web2: 10.0.0.6| 
| Web3: 10.0.0.8| 

Beats have been installed on these machines:

- Web1, Web2, Web3

These Beats allow us to collect the following information from each machine:

- Filebeat allows insight into system logs, NGINX, MySQL, Auditd.
- Metricbeat can record metrics from system, Docker, MongoDB or Kubernetes.

### Using the Playbook

In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:

- Copy either [filebeat-playbook.yml](./filebeat-playbook.yml) or [metric-playbook.yml](./metric-playbook.yml) file to `/etc/ansible/roles`.
- Update the [filebeat-config.yml](./filebeat-config.yml) and [metricbeat-config.yml](./metricbeat-config.yml) file to include target internal IP addresses.
- Run the playbook, and navigate to Kibana to check that the installation worked as expected.

- Playbooks found in: `/etc/ansible/roles`.
- _Specify target machines by updating: ``filebeat-config.yml`
- Kibana (ELK-VM) `http://(current public IP):5601/app/kibana` - Kibana>Add Log/Metric Data>System Logs/Metrics/System Metrics Dashboard (to view logs and metrics) 

### Additional Commands:
- Download `filebeat-config.yml` template:
```
curl https://gist.githubusercontent.com/slape/5cc350109583af6cbe577bbcc0710c93/raw/eca603b72586fbe148c11f9c87bf96a63cb25760/Filebeat > filebeat-config.yml
```
- Download `metricbeat-config.yml` template:
```
curl https://gist.githubusercontent.com/slape/58541585cc1886d2e26cd8be557ce04c/raw/0ce2c7e744c54513616966affb5e9d96f5e12f73/metricbeat
```
- Run `Filebeat` playbook:
``` ansible-playbook filebeat-playbook.yml ```
- Run `Metricbeat` playbook:
``` ansible-playbook metricbeat-playbook.yml ```

