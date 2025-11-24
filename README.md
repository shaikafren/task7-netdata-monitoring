                                                      Task 7 — Monitor System Resources Using Netdata
     Objective :
 Install Netdata on an EC2 instance and visualize system + app performance metrics in real time.

  Tools Used:
    *Netdata (nightly build v2.8.x)
    *AWS EC2 instance (t2.micro / Ubuntu or Amazon Linux)
    *SSH terminal
 
STEPS PERFORMED:
 STEP1:Launch EC2 Instance
 Instance type: t3.micro
 OS: Ubuntu / Amazon Linux
 Open port 19999 in the Security Group.

STEP2: INSTALL NETDATA
   sudo bash <(curl -Ss https://my-netdata.io/kickstart.sh)
   Netdata auto-installed with: 
 Apps Plugin
 System metrics
 Kernel metrics
 Disk, memory, CPU
 Alerts + Notifications
 Web dashboard   
STEP3: ACCESS DASHBOARD
  OPENED IN BROWSER 
               HTTP://35.175.133.155:19999

            Dashboard showed:

CPU usage
RAM consumption
Disk I/O
Network traffic
Running processes
Systemd logs
Alerts & notifications
Containers (if available)
  
STEP4: VERIFIED SYSTEM INFO 
    From dashboard:
CPU: 2 cores
RAM: ~914MB
Disk: 8 GB
OS Kernel: 6.14.0-1015-aws
Netdata version: v2.8.0-nightly
Metrics collected: 884

INTERVIEW QUESTION AND ANSWERS
1. What does Netdata monitor?
A.Netdata monitors live system and application metrics, including:
CPU, RAM, Disk I/O
Network traffic
System processes
Docker containers
Databases, web servers, applications
Kernel metrics, cgroups
Alerts, logs, timers
It is designed for real-time (per-second) monitoring.

2. How do you view real-time metrics?
A.You view real-time metrics using Netdata’s we
 http://35.175.133.155:19999
  metrices update every second even the page is not refieshed.
3.How is Netdata different from Prometheus? 
Netdata = real-time troubleshooting
Prometheus = long-term monitoring + alerting architecture
4. What is a collector?
A.A collector is a plugin or module in Netdata that collects metrics from:
System (CPU, RAM, disk, network)
Applications
Services (NGINX, MySQL, Redis, Docker)
Hardware
Netdata uses plug-ins like:
apps.plugin
proc.plugin
python.d.plugin.
5. What are some performance KPIs to watch?
A.Important KPIs:
CPU usage
Memory usage
Disk I/O latency
Network throughput
Load average
Container resource consumption
Error rates
Application response time
6.How to deploy Netdata on a VM?

A.Simplest method (Linux):

sudo bash <(curl -Ss https://my-netdata.io/kickstart.sh)


Then view dashboard:

  http://35.175.133.155:19999

you can also deploy using:
Docker
Kubernetes helm chart
Manual installation
Netdata Cloud
7.How does Netdata alerting work?
A.Netdata includes built-in alert rules for system metrics.
Alerts are defined in YAML config files.
Alerts can trigger notifications through:
Email
Slack
Discord
PagerDuty
Webhooks
8.What is a dashboard in this context?
A.The Netdata dashboard is a real-time web UI showing:
Live charts
Metrics grouped by category
Health alerts
System overview
Logs
Container performance
Plugin/collector information
It updates every second, enabling fast troubleshooting.
