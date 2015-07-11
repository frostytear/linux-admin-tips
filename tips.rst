linux-admin-tips
================

Everyday linux admin tips try to remember.
------------------

Author: Anton Lin 
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1. HARDWARE

  #. cpu
  #. mb
  #. ram
  #. harddisk
  #. network card
  #. power
  #. case
  #. monitor
  #. keyboard
  #. mouse

2. RAID

3. LVM

.. _my-reference-label:

Section to cross-reference
--------------------------

This is the text of the section.

It refers to the section itself, see :ref:`my-reference-label`.

4. INSTALLATION

  #. kickstart
  #. drbl
  #. clonezilla

5. PACKAGES
uname -a
cat /etc/issue
rpm or dpkg
yum or apt-get
which
whatis
whereis
#
SECURITY
who
finger
w
tripwire
chkrootkit
rkhunter
iptables
ssh
openvas
snort
guardian
nessus
#
NETWORK
LAN eth0
ADMIN LAN eth0:0 NOTEBOOK IP:192.168.1.92
WAN eth1
man -k interfaces
man 5 passwd
man ifup
#
cat /etc/network/interfaces
auto eth0 eth0:0 eth1
iface eth0 inet static
network 10.0.1.0
netmask 255.255.255.0
broadcast 10.0.1.254
address 10.0.1.10
gateway 10.0.1.1

iface eth0:0 inet static
network 192.168.1.64
netmask 255.255.255.192
broadcast 192.168.1.127
address 192.168.1.68
#
cat /etc/sysconfig/network
NETWORKING=yes
NETWORKING_IPV6=no
HOSTNAME=web.ridizain.net
GATEWAY=10.0.1.1
#
vim /etc/sysconfig/network-scripts/ifcfg-eth0#:0
DEVICE=eth0#:0
ONBOOT=yes
TYPE=Ethernet
BOOTPROTO=static
HWADDR=74:27:EA:4C:E5:A7
NETWORK=10.0.1.0
IPADDR=10.0.1.10
PREFIX=24
USERCTL=no
#
You should set the DNS server provide from your ISP.
cat /etc/resolv.conf
search ridizain.net
nameserver 10.0.1.2
nameserver 168.95.1.1
nameserver 8.8.8.8
nameserver 8.8.4.4
#
cat /etc/hostname
cat /etc/hosts
#
ifconfig eth0 192.168.1.68 netmask 255.255.255.192
route -n
route del default gw 192.168.1.1
route add default gw 192.168.1.65
ping
netstat -tunlp
traceroute
tcpdump
vpnc
pppoe
#
SERVICES
cat /etc/services
service --status-all
update-rc.d <service> defaults 
update-rc.d <service> start 20 3 4 5 
update-rc.d -f <service> remove
chkconfig --add <service> 
chkconfig --level 345 <service> on 
chkconfig --del <service>
chkconfig --level 345 NetworkManager off
chkconfig --level 345 network on

ntpdate time.stdtime.gov.tw
ntpdate watch.stdtime.gov.tw
ntpdate clock.stdtime.gov.tw
ntpdate tick.stdtime.gov.tw
ntpdate tock.stdtime.gov.tw

/etc/init.d/apache2 status
service apache2 status
#
KVM
#
SHELL
fc
history
cat
more
less
head
tail
diff
grep
find
#
MONITORING
ntop
nagios
top
df -h
du -sh
#
BACKUP
cpio
tar
dd
dump
restore

