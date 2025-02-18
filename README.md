# NWT

#VLAN EINSTELLEN FÜR EINE SCHNITSTELLE 

enable 

conf t 

interface fastEthernet0/3 

switchport mode access 

switch access vlan 20 

exit 

 

#VLAN EINSTELLEN FÜR MEHR SCHNITSTELLE 

enable 

conf t 

interface range fastEthernet0/1-3 

switchport mode access 

switch access vlan 20 

exit 

 

#VLAN TRUNK MACHEN 

enable 

conf t 

interface fastEthernet0/3 

switchport mode trunk 

switch access vlan 20 

exit 
 
#VLAN NAME 

enable 

configure terminal 

vlan 10 

name Sales 

 

#ROUTER ZEUGS KP 

enable 

conf t 

interface fastEthernet0/1 

no sh 

exit 

 

#SUB INTERFACE??? 

enable 

conf t 

interface fastEthernet0/1.01 

encapsulation dot1Q 10 

ip address 192.160.10.1 255.255.255.0 

exit 
