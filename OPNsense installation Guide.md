### Prerequisties:
The recommended specification to run OPNsense standard features,means every feature is functional and meet the most use cases: 
| Hardware |Sizing|
| ------ | ------ |
| Processor | 1 GHz dual core cpu |
| RAM | 1 GB |
| Install method | DVD |
| install target | 40 GB SSD, a minimum of 1 GB memory is needed for the installer to run. |
### Setup:
```sh
  - Go to OPNsense website and download installation iso through the following link:
  https://opnsense.org/download/
  ```
```sh
  - Open VM ware ESXI and go to Networking then 
    -Go to virtual switches and creat 2 virtual switches for example there names is LAN_Vswitch and WAN_Vswitch. new port groups and relate the the port groups with the v_switches 
    for example the port groups names will be :
        lAN_Port_Group and relate it to LAN_Vswitch.
        WAN_Port_Group and relate it to WAN_Vswitch.
```
```sh
    -Go to virtual machines and creat new virtual new virtual machine for OPNsense firewall and assgin the Prequesites as mentioed above and upload the instllation iso on the ESXI the click finish.
```
- ### Open the OPNsense and Start installation which is:
```sh
-Accept the sttings.
 Select Guided installation.
-select Disk .
-select installation mode.
-Swap partition.
-The OPNsense will start executing the commands.
-Set Root password
-Reboot OPNsense 
```
- ### After the reboot there are 13 options will appear which is
```sh
0 Logout
1 Assgin interfcaes
2 Set interface ip address
3 Reset the root password 
4 Reset the factory defaults
5 Power off system
6 Reboot System
7 Ping Host
8 Shell
9 Pftop
10 Firewall Log
11 Reload all the sevices
12 Update from Console
13 Restore and Backup
```
- Press 2 to assgin the IP addresses for the LAN and WAN interfaces
  for every interface you cant set :
```sh
IPv4 address
Subnet Mask 
The Gateway
IPv6 address
DNS server 
```

### Start OPNsense GUI:
- TO open the OPNsense GUI you have 2 options :
1-Acess from the LAN :
here you type the ip address of the LAN interface in your web browser and use the Root username and password to login OPNsense.
2-Acess from the WAN :
you have to go to shell first and run the following command to enable access from the WAN
```sh
pfctl -d
```
then type the the ip address of the WAN interface in the web browser and use Root username and password to login.