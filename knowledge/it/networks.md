# networks

### network configuration

* using ip `$ ip a`
* using ifconfig `$ ifconfig`
* using nmcli \(networkmanager\) `$ nmcli device show`

### Enable/disable interfaces

* using ifdown e ifup \# `ifdown eth0 && ifup eth0`
* using ip `# ip link set dev eth0 down && ip link set dev eth0 up`
* using networking \(deprecated\) `# service networking restart`
* using network restart `# /etc/init.d/network restart`
* using ifconfig `# ifconfig eth0 down && ifconfig eth0 up`

### scan devices

* using nmap `$ sudo nmap -sn 192.168.0.0/24`

### using ip command

* show all interfaces configuration `$ ip a`
* add an ip to an interface \(not persistent\) `$ ip a add 192.168.0.1/24 dev eth0`
* Remove an ip from an interface `$ ip a del 192.168.0.1/24 dev eth0`
* deactivate an interface `$ ip link set dev eth0 down`
* activate an interface `$ ip link set dev eth0 up`
* modifying a MAC address of an interface \(interface must be deactivated\) `$ ip link set dev eth0 address 00:0c:13:45:5b:b6`
* add default route \(default may be replaced by 0/0\) `$ ip route add default via 192.168.0.254`
* add a static route to a subnetwork `$ ip route add 10.0.0.0/24 via 192.168.0.254 dev eth0`
