## Investigation Evidence

ip.addr == 45.131.214.85

### Command and Control Communication

Filtering traffic for the malicious IP address revealed communication between the infected host and the NetSupport Manager RAT infrastructure.

Wireshark Filter:
ip.addr == 45.131.214.85



2️⃣ Hostname Discovery

### Hostname Discovery via NBNS

NetBIOS Name Service traffic was analyzed to identify the hostname of the infected Windows client.

Wireshark Filter:
nbns

DESKTOP-TEYQ2NR


3️⃣ MAC Address Identification

### MAC Address Identification

Frame details in Wireshark were examined to identify the MAC address of the infected system.

The MAC address was extracted from the Ethernet II header.

Ethernet II
Source: 00:19:d1:b2:4d:ad


4️⃣ User Account Identification


kerberos.CNameString

### User Account Identification

Kerberos authentication traffic was analyzed to determine the user account associated with the infected system.

Wireshark Filter:
kerberos.CNameString


brolf


### Full Name Identification


Search packet details for: brolf


Becka Rolf