# Blue Team: Summary of Operations

## Table of Contents

- Network Topology
- Description of Targets
- Monitoring the Targets
- Patterns of Traffic & Behavior
- Suggestions for Going Further

### Network Topology

The following machines were identified on the network:

- Name of VM 1
  - **Operating System**: Kali Linux
  - **Purpose**: Attack Machine
  - **IP Address**: 192..168.1.90
- Name of VM 2
  - **Operating System** Linux
  - **Purpose**: Elasticsearch (ELK)
  - **IP Address**: 192.168.1.100
- Name of VM 3
  - **Operating System** Microsoft
  - **Purpose**: Capstone Webserver
  - **IP Address**: 192.168.1.105
- Name of VM 4
  - **Operating System** Linux
  - **Purpose**: Target Machine 1 (Webserver)
  - **IP Address**: 192.168.1.110
- Name of VM 5
  - **Operating System** Linux
  - **Purpose**: Target Machine 2 (Webserver)
  - **IP Address**: 192.168.1.115


### Description of Targets

The target of this attack was: Target 1 - 192.168.1.110

Target 1 is an Apache web server and has SSH enabled, so ports 80 and 22 are possible ports of entry for attackers. As such, the following alerts have been implemented:

### Monitoring the Targets

Traffic to these services should be carefully monitored. To this end, we have implemented the alerts below:

#### Name of Alert 1

Excessive HTTP Errors is implemented as follows:

  - **Metric**: http.response.status_code
  - **Threshold**: Above 400 for the last 5 minutes
  - **Vulnerability Mitigated**: DDOS Attack, Brute-Force
  - **Reliability**: medium

#### Name of Alert 2

HTTP Request Size Monitor is implemented as follows:

  - **Metric**: http.request.bytes
  - **Threshold**: If above 3500 for the last 1 minute
  - **Vulnerability Mitigated**: Backdoor,Command-and-Control, Brute-Force
  - **Reliability**: low

#### Name of Alert 3

CPU Usage Monitor is implemented as follows:

  - **Metric**: system.process.cpu.total.pct
  - **Threshold**: Above 0.5 for the last 5 minutes
  - **Vulnerability Mitigated**: Command-and-Control
  - **Reliability**: low
