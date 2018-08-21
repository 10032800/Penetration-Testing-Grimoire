# Initial Host Discovery and Fingerprint Scans
This cheat sheet should be used as a guidline for host discovery and sevice fingerprinting during the penetratino tests.
## Host Scan / Discovery Methodology
Below are the enumeration steps that should be taken on every system during the penetration test. These steps can be adjusted according to the penetration test type, black box/etc.
### Scan the device for services:
1. __Nmap__ with service enumeration enabled.
### Scan for shares and WINDOWS data:
1. __NBTScan__ look for open shares on the target 
2. __Enum4Linux__ look for data from Windows hosts and LINUX Samaba hosts
### Web Services / Apps
1. __Nikto__ scan for vulnerabilities
2. Browse to them and poke around for vulnerabilities
3. __SQLMap__ scan if any GET or POST input was found in the manual tests
## Service Enumeration and Fingerprinting
This section of this module will focus on the service scanning and techniques on how to get service information to be used for vulnerability analysis on the target system.
### NMAP
Initial `nmap` scan should be done without specifying a port range but adding service fingerprinting as,

`nmap -A (target IP address)`

This type of scan takes a considerable amount of time to complete.
