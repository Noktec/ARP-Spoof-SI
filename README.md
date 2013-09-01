ARP Spoof SI is an application that uses ARP packets for creating a
Man In The Middle (MITM) attack.

Copyright (C) 2012  Antonin Beaujeant

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.


REQUIREMENTS
------------

This program requires:

      libpcap - http://www.tcpdump.org/
      libnet - http://libnet.sourceforge.net/

Built and tested on Ubuntu 10.10 and OS X Lion.


INSTALL
-------

Compile with gcc:

```	
$ gcc $(libnet-config --defines) -o arp_spoof_si arp_spoof_si.c -lnet -lpcap
```


USAGE
-----
```
$ sudo ./arp_spoof_si <IP target 1> <IP target 2> [OPTIONS]
```


[OPTIONS]
	-i interface : Select the interface


Examples:
```	
sudo ./arp_spoof_si 192.168.1.1 192.168.1.10
sudo ./arp_spoof_si 10.0.1.99 10.0.1.1 -i eth1
```
