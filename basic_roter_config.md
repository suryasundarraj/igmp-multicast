**On Router 1**

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

**On Router 2**

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

**On Router 3**

```
config terminal
interface FastEthernet 0/0
ip address 2.0.0.3 255.0.0.0
no shutdown
exit
interface FastEthernet 0/1
ip address 192.168.2.3 255.255.255.0
no shutdown
exit
interface FastEthernet 1/0
ip address 192.168.4.3 255.255.255.0
no shutdown
exit
interface FastEthernet 1/1
ip address 192.168.3.3 255.255.255.0
no shutdown
exit
router ospf 1
network 2.0.0.0 0.255.255.255 area 0
network 192.168.2.0 0.0.0.255 area 0
network 192.168.4.0 0.0.0.255 area 0
network 192.168.3.0 0.0.0.255 area 0
exit
exit
wr
```

**On Router 4**

```
config terminal
interface FastEthernet 0/0
ip address 192.168.5.4 255.255.255.0
no shutdown
exit
interface FastEthernet 0/1
ip address 192.168.7.4 255.255.255.0
no shutdown
exit
interface FastEthernet 1/0
ip address 192.168.4.4 255.255.255.0
no shutdown
exit
interface FastEthernet 1/2
ip address 192.168.6.4 255.255.255.0
no shutdown
exit
router ospf 1
network 192.168.5.0 0.0.0.255 area 0
network 192.168.7.0 0.0.0.255 area 0
network 192.168.4.0 0.0.0.255 area 0
network 192.168.6.0 0.0.0.255 area 0
exit
exit
wr
```

**On Router 5**

```
config terminal
interface FastEthernet 0/0
ip address 1.0.0.5 255.0.0.0
no shutdown
exit
interface FastEthernet 0/1
ip address 192.168.7.5 255.255.255.0
no shutdown
exit
interface FastEthernet 1/0
ip address 192.168.8.5 255.255.255.0
no shutdown
exit
interface FastEthernet 1/2
ip address 192.168.6.5 255.255.255.0
no shutdown
exit
router ospf 1
network 1.0.0.0 0.255.255.255 area 0
network 192.168.8.0 0.0.0.255 area 0
network 192.168.7.0 0.0.0.255 area 0
network 192.168.6.0 0.0.0.255 area 0
exit
exit
wr
```

**On Router 6**

```
config terminal
interface FastEthernet 0/0
ip address 192.168.5.6 255.255.255.0
no shutdown
exit
interface FastEthernet 1/1
ip address 192.168.3.6 255.255.255.0
no shutdown
exit
interface FastEthernet 1/2
ip address 192.168.6.6 255.255.255.0
no shutdown
exit
router ospf 1
network 192.168.5.0 0.0.0.255 area 0
network 192.168.3.0 0.0.0.255 area 0
network 192.168.6.0 0.0.0.255 area 0
exit
exit
wr
```

**On Router 7**

```
config terminal
interface FastEthernet 0/0
ip address 1.0.0.7 255.0.0.0
no shutdown
exit
router ospf 1
network 1.0.0.0 0.255.255.255 area 0
exit
exit
wr
```
