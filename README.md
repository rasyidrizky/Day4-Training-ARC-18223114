# Day4-Training-ARC-18223114
Konfigurasi Basic Network dengan Cisco Packet Tracer

## Addressing Table
Berikut konfigurasi interface yang digunakan setiap device
| **Device** | **Interface** | **IP Address**           | **Default Gateway** |
|------------|---------------|--------------------------|---------------------|
| College    | Gig0/0        | 10.10.10.1/24            | N/A                 |
|            |               | 2001:DB8:ACAD:100::1/64  | N/A                 |
|            | Gig0/1        | 10.10.11.1/24            | N/A                 |
|            |               | 2001:DB8:ACAD:200::1/64  | N/A                 |
| Class-A    | VLAN 1        | 10.10.10.100/24          | 10.10.10.1          |
| Class-B    | VLAN 1        | 10.10.11.100/24          | 10.10.11.1          |
| Student-1  | NIC           | 10.10.10.101/24          | 10.10.10.1          |
|            |               | 2001:DB8:ACAD:100::50/64 | FE80::2             |
| Student-2  | NIC           | 10.10.10.102/24          | 10.10.10.1          |
|            |               | 2001:DB8:ACAD:100::60/64 | FE80::2             |
| Student-3  | NIC           | 10.10.11.101/24          | 10.10.11.1          |
|            |               | 2001:DB8:ACAD:200::50/64 | FE80::3             |
| Student-4  | NIC           | 10.10.11.102/24          | 10.10.11.1          |
|            |               | 2001:DB8:ACAD:200::60/64 | FE80::3             |

## Additional Configuration
Berikut konfigurasi tambahan yang dilakukan sebagai penyempurnaan tugas
```bash
Console line password: cisco
Secret password: class
```

## Switch Class-B
```bash
hostname Class-B
interface Vlan1
description This is a VLAN1 port
banner motd # Welcome to the Class-B Switch #
```

## Router College
```bash
hostname College
interface GigabitEthernet0/0
description This is a port to Subnet A

interface GigabitEthernet0/1
description This is a port to Subnet B
banner motd # Welcome to the College Router #
```