# dhcp-vlan-config


## router

ip dhcp excluded-address 172.16.1.0 172.16.1.5

ip dhcp excluded-address "ip cim ettöl" - "ip cim eddig"

ip dhcp excluded-address Low IP address - High IP address


ip dhcp pool valami

network 172.16.1.0 255.255.255.0

network "ip cim tartomány" és "mask"

default-router 172.16.1.1 

default-router "ip cim"

dns-server 8.8.8.8

________________________________________
en 
conf t

ip dhcp excluded-address 172.16.1.0 172.16.1.5

ip dhcp pool valami

network 172.16.2.0 255.255.255.0

default-router 172.16.2.1 

dns-server 8.8.8.8

ex

int g0/0.10

encapsulation dot1Q 10

ip address 172.16.1.1 255.255.255.0
ex
int g0/0.20

enc dot1q 20

ip address 172.16.2.1 255.255.255.0


ex

## switch
en
conf t
vlan 10
name vencel_buzi
ex
int range f0/1-5
sw mode acces 
sw acces vlan 10

ex
vlan 20
name hunor
ex

int range f0/6-15
sw mode acces
sw acces vlan 20
ex
