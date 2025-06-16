# What Is Port Security
### Description
**Port security** is a feature on Cisco switches that allows network administrators **to control which devices can connect to specific switch ports**. By associating allowed devices with their MAC addresses, port security helps **prevent unauthorized access** and **mitigate potential security threats**.

### How To Configure Port Security
- Enable port security: 
```bash
switchport port-security
```

- Set Maximum Allowed MAC Addresses:
```bash
switchport port-security maximum [number]
```

- Manually Assign Secure MAC Addresses:
```bash
switchport port-security mac-address [MAC address]
```

- Enable Sticky MAC Address Learning (means first MAC-address learned, is the one that only allowed in this port):
```bash
switchport port-security mac-address sticky
```

- Configure Violation Mode (when an unauthorized device tries to use a port):
```bash
switchport port-security violation [mode]
```
modes include:<br>
**shutdown:** Disables the port upon violation.<br>
**restrict:** Drops packets from unauthorized devices and logs the violation.<br>
**protect:** Drops packets from unauthorized devices without logging.

- To verify port security configurations:
```bash
# for general configuration informations
show port-security

# for a port-specific details use
show port-security interface [interface-id]
```




