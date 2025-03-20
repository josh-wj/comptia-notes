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
> - Proxy server Forward/Reverse
> - Intrusion Prevention System (IPS)/Intrusion Detection System (IDS)
> - Load balancer
> - Sensors

### Port Security
> vital for safeguarding network access and preventing unauthorized devices from communicating through network ports

> - The 802.1X authentication standard provides port-based network access control
> - EAP (extensible access protocol) is a universal authentication framework that defines message formats. It’s frequently used with 802.1X
> - **_PEAP_**
> - EAP-FAST
> - **EAP-TLS**
> - EAP-TTLS

### Firewall
> a network security device or software that acts as a barrier between a trusted internal network and untrusted external networks such as the Internet

   Types
>    - WAF ( Web application Firewall )
>    - NGFW ( Next Generaation Firewall)
>    - UTM ( more than a firewall but considered one )
>    - Understand TLS inspection (seperate concept )

### VPN
> establishes a secure connection between two or more devices over the Internet, even if they are not on the same private network
> - L2TP
> - IPSEC
> - Transport ( understand AH ) vs. Tunnel mode ( understand ESP )

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
> - IKE ( Internet Key Exchange ), the key management protocol for IPsec, has two phases. Phase 1 negotiates the ISAKMP SA, and Phase 2 negotiates the IPsec Sas

### Software-Defined Wide Area Network (SD-WAN)
> a networking architecture that uses software-based controls to optimize and manage data traffic across a wide-area network (WAN)

> - Enhances network management flexibility by separating control mechanisms from network hardware
> - Simplifies network management, improves performance, and enhances reliability
### Secure Access Service Edge (SASE)
> a cloud-native architecture that merges network security functions with WAN capabilities

> - Integrates network and security services into a unified platform, simplifying management and ensuring secure access 
> - Provides secure and seamless access to resources regardless of user location

**important** 
fail open/closed
load balancing 
802.1X
EAP/PEAP
NGFW, TLS inspection
VPN L2TP IPSEC
SD-WAN
SAEC



## Chapter 12
**Topics**
> - Data types
> - Data Classification
> - General Data Considerations
   > - Data States
   > - Data Sovereignty
   > - Geolocation
> - Methods to Secure Data
    Geographic Restrictions
    Encryption
    Hashing
    Masking
    Tokenization
    Obfuscation
    Segmentation
    Permission Restrictions

### Data Types

Regulated Data
> Subject to laws and regulations due to sensitivity, such as medical records regulated by HIPAA

Trade secret
> Confidential information providing a competitive advantage, like a proprietary algorithm

Intellectual property (IP)
> Protected creative works, inventions, and designs, including copyrighted source code

Legal information
> Data related to legal processes or obligations, such as signed contracts or employee agreements

Financial information 
> Data concerning financial operations and performance, regulated by laws like SOX and GLBA, including balance sheets, income statements, and tax records

Human- and non-human-readable data
> Human-readable data (e.g., text documents) and non-human-readable data (e.g., encrypted files)

### Data Classifications

Confidential or proprietary
> Information or assets that could cause grave damage to an organization if accessed without authorization

Sensitive
> Data that could cause some damage to an organization if accessed without authorization

Public
> Information openly available without causing harm or presenting risks if exposed

Private
> Information or assets that could cause severe damage to an organization if accessed without authorization (e.g., payroll data)

Restricted
> Data requiring the highest level of security measures due to its sensitive nature or stringent legal obligations

Critical
> Data essential to the continued function of a business, the loss of which would result in significant monetary loss for the organization

### General Data Considerations

Data states
> The states in which data exists: at rest, in transit, and in use

Handling procedures
> Establish clear procedures for handling data throughout its lifecycle, from creation and storage to sharing and disposal

Security measures
> Implement robust security measures, including encryption, access controls, monitoring, and incident response protocols to help safeguard data against unauthorized access, breaches, and other security threats

### Data Sovereignty & Geolocation

Data sovereignty
> -  Legal and regulatory requirements for data based on its collection or processing location
> -  Mandates often dictate that data must remain within a country's borders

Geolocation
> - Identification or estimation of real-world geographic location based on digital information
> - Uses technologies like GPS tagging, geofencing, and IP-based location services

### Methods to Secure Data

Geographic Restriction
> Limits access to data based on user's geographic location

Encryption
> Converts readable data to an encoded format

Hashing
> Converts data to fixed-length strings for verifying integrity

Masking
> Replaces specific data with fictitious but structurally similar data

Tokenization
> Replaces sensitive information with a placeholder, reducing the risk of data breaches

Obfuscation
> Makes data unintelligible without affecting functionality

### Segmentation
> Divides a network into segments that isolate data

EX.
> - Finance segment: Highly secure area of the network for sensitive financial information
> - Firewall segment: Also known as a screened subnet; a buffer zone between the external network (Internet) and internal network
> - Engineering segment: Isolated environment for development and testing purposes
> - Sales segment: For customer relationship management (CRM) systems, sales records, and customer-related data

### Permision Restriction
> specify who can perform which actions within a system or network

Methods
> - Role-based access control (RBAC): Access permissions are assigned to organizational roles
> - Attribute-based access control (ABAC): Access is granted based on attributes like location, time, or device type.
> - Principle of least privilege: Ensures that users have only the minimum access necessary to perform their tasks















































































































































































































































































































