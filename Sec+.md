## chapter_11

### Infrastructer conditions
   - Device placement
   - Security Zones
   - Attack Surface
   - Connecrivity
   - failure Modes
   - Device Attributes
   - Server Communications/Access
   - Network Applications
   - Port Security
   - Firewall Types
### Secure Communications/Access
   - Virtual Private network (VPN)
   - Remote Access
   - Tunneling
   - Software Defined Wide Area Network (SD-WAN)
### Device Placement
   > Is the thoghtful positioning of hardware devices within a network
#### Considerations
       - Security Requirments
       - Network Efficiency
       - Accessability
#### Examples
      - Place firewalls close to the network perimeter to prevent unauthorized access
      - Position sensitive data servers in secure locations to minimize exposure to threats

### Security zones
> Segragated areas in a network under specific security policies and controls

    Internal zones
    > Trusted segments in which sensitive or internal data is proccessed
    
    External Zones
    > Areas allowing connections from public internet or other untrusted networks
    
    Screened Subnet
    > Specialized external zone that isolates public-facing services from the internet
    
    Specialized Zones
    > Zones designed to meet regulatory compliance requirments\

### Attack Surface
> All the vulns. and potential access points an attacker could use to gain access to the system

Larger Surface = Greater Risk

**Strategies to reduce the attack surface**
> - Turn off unnecessary services
> - Close open ports
> - Apply patches and updates
> - Use firewalls
> - Implement strong authentication
    
### Connectivity
> How network, systems, and apps. aonnect and communicate\

**Security considerations**
> - Encrypt data in transit
> - Secure connection endpoints
> - Employ secure protocols
> - Use VPNs or firewalls\

Remember connectivity when desighning new systems with other departments

### Failure Modes
> how a system responds when a portions fails\

**Fail-open Configurations**
> System remains available if a portion fails

**Fail-Closed Configuration**
> Entire system becomes inaccessible if a portion fails

**EX.**
   - DNS server: May fail open to continue servicing other zones, but the database server may fail closed to protect confidential information
   - Firewall: Would fail closed to maintain security

### Device Attributes
> A characteristic determining device operation in a network environment

**Active vs. Passive**
 > - Active/active: Devices share workload simultaneously; critical for failover or load balancing
 > - Active/passive: One device active, another on standby; passive activates if active fails or is manually switched

**Inline monitoring vs. tap/monitor mode**
> - Inline monitoring: Device is placed directly in traffic flow, allowing active intervention
> - Tap/monitor mode: Device observes traffic without  interfering

### Network Appliances
> Essential for network functionality , security, and efficiency

**Types of network appliences**
> - Jump server
> - Proxy server
> - Intrusion Prevention System (IPS)/Intrusion Detection System (IDS)
> - Load balancer
> - Sensors

### Port Security
> vital for safeguarding network access and preventing unauthorized devices from communicating through network ports

> - The 802.1X authentication standard provides port-based network access control
> - EAP is a universal authentication framework that defines message formats. It’s frequently used with 802.1X

### Firewall
> a network security device or software that acts as a barrier between a trusted internal network and untrusted external networks such as the Internet

### VPN
> establishes a secure connection between two or more devices over the Internet, even if they are not on the same private network

### Remote Access
> allows authorized users to connect to a network, system, or application from a location outside the organization's physical premises

**Remote access technologies**
> - Remote Access Service (RAS)
> - Virtual Private Networks (VPNs)
> - Terminal Access Controller Access Control System Plus (TACACS+)
> - Challenge-Handshake Authentication Protocol (CHAP)

### Tunneling
> creates a secure pathway for data transmission across networks via encapsulation

> - Protocols like Transport Layer Security (TLS) and Internet Protocol Security (IPsec) enhance the security of tunneling by providing encryption and integrity mechanisms
> - IKE, the key management protocol for IPsec, has two phases. Phase 1 negotiates the ISAKMP SA, and Phase 2 negotiates the IPsec Sas

### Software-Defined Wide Area Network (SD-WAN)
> a networking architecture that uses software-based controls to optimize and manage data traffic across a wide-area network (WAN)

> - Enhances network management flexibility by separating control mechanisms from network hardware
> - Simplifies network management, improves performance, and enhances reliability

### Secure Access Service Edge (SASE)
> a cloud-native architecture that merges network security functions with WAN capabilities

> - Integrates network and security services into a unified platform, simplifying management and ensuring secure access 
> - Provides secure and seamless access to resources regardless of user location

## Chapter 12


















































































































































































































































































































































































