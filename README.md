# Uses ctypes to get the IP configuration

## pip install ipinfooo

#### Tested against Windows 10 / Python 3.10 / Anaconda


I haven't written a single line of this code, and I don't know who wrote it. But I know that it is pretty useful if you need details about your network connection - Mozilla Public License, v. 2.0.

From the source code:

```python

#  For the sake of humanity here's a python script retrieving
#  ip information of the network interfaces.
#
#  Pay some tribute to my soul cause I lost a few years on this one
#
#  based on code from jaraco and many other attempts
#  on internet.
#  Fixed by <@gpotter2> from scapy's implementation to
#  add IPv6 support + fix structures
#
#  This Source Code Form is subject to the terms of the Mozilla Public
#  License, v. 2.0. If a copy of the MPL was not distributed with this
#  file, You can obtain one at http://mozilla.org/MPL/2.0/.\
#
```


```python
from ipinfooo import get_win_ifaddrs
get_win_ifaddrs()
Out[4]: 
[{'Realtek Gaming GbE Family Controller': {2: {'addr': 'xxx',
    'netmask': 'xxx',
    'broadcast': 'xx255',
    'network': '1xxxx0'}}},
 {'VirtualBox Host-Only Ethernet Adapter': {2: {'addr': '192.168.56.1',
    'netmask': '255.255.255.0',
    'broadcast': '192.168.56.255',
    'network': '192.168.56.0'},
   23: {'addr': 'xxxx',
    'netmask': 'ffff:ffff:ffff:ffff::',
    'broadcast': 'fe80::ffff:ffff:ffff:ffff',
    'network': 'fe80::'}}},
 {'Software Loopback Interface 1': {2: {'addr': '127.0.0.1',
    'netmask': '255.0.0.0',
    'broadcast': '127.255.255.255',
    'network': '127.0.0.0'},
   23: {'addr': '::1',
    'netmask': 'ffff:ffff:ffff:ffff:ffff:ffff:ffff:ffff',
    'broadcast': '::1',
    'network': '::1'}}}]
```