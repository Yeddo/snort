
# Snort Rule Templates

Templates for different scenarios. 

## List of Rule Templates

1. `detect_specific_ip.rules` - Detects traffic from a specific IP address.
2. `detect_specific_port.rules` - Detects traffic on a specific port.
3. `detect_protocol.rules` - Detects traffic using a specific protocol (e.g., ICMP).
4. `detect_payload_content.rules` - Detects traffic containing specific content in the payload.
5. `detect_source_and_dest.rules` - Detects traffic from a specific source IP to a specific destination IP and port.

## How to Use

1. Modify the IP addresses, ports, protocols, or content within the rules to fit your network environment.
2. Save the modified rules in your Snort configuration directory.
3. Reload or restart Snort to apply the new rules.

### Example

To detect HTTP traffic on port 80 from a specific IP, modify the `detect_specific_ip.rules` template as follows:

```
alert tcp any any -> 192.168.1.100 80 (msg:"HTTP Traffic from Specific IP"; sid:1000006; rev:1;)
```

Save the file and restart Snort to apply the changes.

Happy Snorting!
