The project is implemented in a virtualized lab environment, where all components—
firewall, virtual machines, and switches—are interconnected using virtual network 
infrastructure. This architecture ensures safe testing, isolation, and full control over traffic 
flow without affecting a physical production network.
The virtual network is designed using three FortiGate physical interfaces, each mapped to 
separate virtual switches:
Port1 → WAN_ext Switch:
Acts as the external/shared network between all components. It provides the base 
communication environment and simulates an external WAN connection.
Port2 → vSwitch_Admin:
Connected to the Admin VM (Windows/Linux). This network segment is considered the 
protected internal environment where critical resources reside.
Port3 → vSwitch_Attacker:
Connected to the Kali Linux attacker VM. This segment serves as the testing and attack zone 
used for penetration testing, scanning, and malicious simulation.
This segmented architecture enables proper network isolation, traffic control, and threat 
detection. Traffic between the attacker VM and the admin VM must pass through the 
FortiGate firewall, ensuring that all interactions are inspected, logged, allowed, or blocked 
based on configured security policies.
The use of a virtualized setup allows safe execution of malware tests, vulnerability scans, and 
exploitation attempts, ensuring realistic security evaluation without risking actual production 
systems
