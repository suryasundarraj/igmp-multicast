** On Router 1 **

```
config terminal
interface FastEthernet 0/0
ip address 2.0.0.1 255.0.0.0
no shutdown
exit
router ospf 1
network 2.0.0.0 0.255.255.255 area 0
exit
exit
wr
```

** On Router 2 **

```
config terminal
interface FastEthernet 0/1
ip address 192.168.2.2 255.255.255.0
no shutdown
exit
interface FastEthernet 1/0
ip address 192.168.8.2 255.255.255.0
no shutdown
exit
interface FastEthernet 1/2
ip address 192.168.6.2 255.255.255.0
no shutdown
exit
router ospf 1
network 192.168.2.0 0.0.0.255 area 0
network 192.168.6.0 0.0.0.255 area 0
network 192.168.8.0 0.0.0.255 area 0
exit
exit
wr
```
