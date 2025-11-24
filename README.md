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

