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

### **important/homework** 
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

### **important/homework**
regulated data
intellectual property
data states
obsfucation
masking
data classifications and types

## chapter 13

**Topics**
> - High Availability
> - Site Considerations
> - Platform Diversity
> - Multi-Cloud System
> - Continuity of Operations
> - Capacity Planning
> - Testing
> - Backups
> - Power


### High Availability ( H.A )
> ensures that a system or application remains accessible and operational over an extended period

> - Redundant hardware\
> Multiple instances of critical hardware components eliminate single points of failure

>- Automated backups\
> Regularly scheduled backups are automated to ensure that the most recent data is always available for recovery

>- Failover mechanisms
> Configuration allows the system or network to switch to a standby system or network automatically if the primary one fails

### Cloud Environments
> In cloud computing, availability is often determined by the storage class
>- Different availability metrics influence cost
>- Storage class selection should be based on a thorough risk analysis
>- Recommendation: Select applications with greater storage availability for mission-critical uses

### Site Considerations
>- Hot site\
>  A near duplicate of the organization’s original site that can be up and running within minutes

>- Warm site\
> Contains computers, phones, and servers but may require configuration before use

>- Cold site\
> Provides basic office infrastructure, but extensive computer configuration and data restoration would be needed before use

>- Geographically distant site\
>  A computing environment, such as a data center, located at least 50 miles from the main compute campus data center

### Platform Diversity
> is the implementation of varied hardware or software platforms within an organization’s IT environment

> Reduces systemic risks associated with a single point of failure

> Benefits
> - Resilience: Increased ability to withstand security incidents and technical failures\
> - Enhanced recovery: Improved capacity to recover from incidents due to diversified platforms

### Multi-Cloud System
> involves using multiple cloud service platforms (e.g., AWS, Azure, Google Cloud) to fulfill diverse computational and storage needs

> Reduces dependency on a single cloud service provider

> Benefits
>- Risk mitigation
>- High availability
>- Robust disaster recovery

### Continuity of Operations
> is a federal initiative encouraging organizations to plan for the continuation of critical operations under various emergency  circumstances

> Procedures in a continuity plan
>- Alerting, activating, notifying, and deploying employees
>- Identifying critical business functions
>- Establishing an alternate facility or work-from-home process
>- Creating a roster of personnel with authority and knowledge of business operational functions
 
### Capacity Planning
> is the process of determining future resource requirements such as people, technology, and infrastructure

> Considerations\
> - People: Staffing requirements to maintain and operate systems efficiently
> - Technology: Computational power, software, and hardware needed to meet future demands
> - Infrastructure: Physical or virtual resources to  support technology and personnel

### Testing
> Tabletop Exercises
> - Validate and improve incident response plans (IRPs) through real-life scenario simulations
> - Gauge team performance against predefined questions and scenarios

> Failover Testing
> - Involves switching operational functions from primary to secondary systems to assess continuity during system failures
> - Tests redundancy mechanisms and contingency plans

> Simulations
> - Provides structured exercises to practice incident response procedures in simulated realistic scenarios
> - Helps identify deficiencies, improve response capabilities, and validate readiness

> Parallel Processing                  
> - Runs same tasks concurrently in primary and secondary systems
> - Verifies backup system's operational reliability and accuracy

### Backups
> A backup is a duplicate copy of data and system configurations stored separately from the original.

> Types of backups
>- Full backup
>- Incremental backup
>- Differential backup
>- Mirror backup
>- Continuous data protection (CDP)
>- Cloud backup
>- Virtual backup
>- Bare-metal backup

### Power
> Power management involves provisioning, controlling, and efficiently utilizing electricity to maintain uninterrupted facility operation.

> Uninterruptible Power Supply (UPS) devices offer emergency power during main power failures by storing energy in batteries or supercapacitors.

> Generators supply power during complete power loss or in areas without standard electrical service, converting mechanical or chemical energy into electrical energy.

### **Important/homework**

## Chapter 14
**Topics**
>- Secure Baselines
>- Hardening Targets
>- Wireless Devices
>- Mobile Solutions
>- Connection Methods
>- Wireless Security Settings
>- Application Security
>- Sandboxing
>- Monitoring

### Secure Baselines
> Secure baselines are standardized sets of minimum configurations and security controls for systems and software.

> Asset tagging
> - Assigning unique identifiers to each asset for easier tracking

> Version control
> - Documenting all software versions used by the organization; helps identify outdated or unsupported versions that may pose security risks

> Scheduled scans
> - Scheduling regular vulnerability scans to identify any new weaknesses  

> Manual review
> - A human reviews data, logs, and systems to help prioritize vulnerabilities based on actual organizational risk. Human judgment and intuition can identify issues that automated tools miss. 

> Disable unnecessary services
> - Turn off services and features not required for the system’s primary function.

> User access control
> - Limit user permissions to what is necessary for their roles.

> Change log
> - Maintain a record of any changes made to the baseline, who made them, and why.

> Audit trail
> - Ensure that documentation is in a format that can be easily audited for compliance purposes.

> Validation testing
> - Confirm that the baseline settings do not disrupt necessary functions.

> Rollback plan
> - Have a plan to revert changes in the event of unforeseen issues during deployment.

> Patch management
> - Regularly update software and systems to patch known vulnerabilities.

> Review and update
> - Periodically review the secure baseline to ensure that it aligns with current best practices in cybersecurity.

### Hardening targets
> the process of strengthening the security defenses of computing resources to resist attacks.

> Common hardening techniques
>- Firmware updates
>- Network segmentation
>- VLANs
>- Air-gapping
>- Disabling unnecessary features
>- Real-time monitoring
>- Data encryption
>- Changing default passwords
>- Ensuring network-level security

### Wireless devices
> Wireless devices operate without physical wired connections. They use methods such as Wi-Fi, Bluetooth, and cellular networks to communicate.

> Site surveys
> - assess the current wireless environment and plan for Wi-Fi network optimization.

> Heat maps
>- visualize wireless activity to determine optimal access point placement for coverage and performance.

### Mobile solutions
> Mobile device management (MDM) is crucial for successful implementation of bring your own device (BYOD) policies.

> BYOD policies raise legal concerns regarding data ownership, privacy rights, and employee misconduct.

> Ensure clear separation of organizational and personal information.

> Encryption, regular software updates, and password complexity are essential for mitigating mobile device security risks.

### Connection Methods
> Bluetooth
> -  is susceptible to attacks like Bluejacking and Bluesnarfing.

> Wi-Fi
> - is vulnerable to various exploits. Example: Firmware flaws that lead to buffer overflow

> Cellular connections
> - including 2G, 3G, 4G, and 5G all raise security concerns. Using newer devices is generally best.

> GPS and geolocation technologies
> - raise privacy and security concerns.

> Satellite communications (SATCOM)
> - require firmware updates to address vulnerabilities and prevent exploits.

> Infrared connections and wireless USB receivers
> - often overlooked in security reviews. 

### Wireless Security Settings
> WPA3 (Wi-Fi Protected Access 3)
> - uses Simultaneous Authentication of Equals (SAE) to replace the vulnerable preshared key (PSK) system.

> RADIUS federation
> - enables secure communication among multiple RADIUS servers.

> Cryptographic protocols
> -  WPA3-Personal and WPA3-Enterprise offer robust encryption methods like AES-CCMP and HMAC-SHA for data protection.

> Authentication protocols
> -  LDAP, Kerberos, and 802.1X are authentication methods tailored to various environments.

### Application Security
> Application security refers to the security measures implemented at the application level.

> Input validation
> - ensures data integrity by verifying the type and content of user or application input, preventing vulnerabilities like XSS and SQLi.

> Secure cookies
> - implement the secure attribute in HTTP response cookies to prevent unauthorized access and transmission of sensitive information.

> Static code analysis uses SAST tools to scan source code for vulnerabilities early in the development lifecycle.
>- Provides real-time feedback to developers 
>- Enables prompt issue resolution

> Code signing digitally signs executables and scripts to verify authenticity and integrity.
>- Ensures software has not been altered or corrupted 
>- Prevents malicious tampering during transmission

### Sandboxing

> Sandboxing creates a confined execution environment for running untrusted or suspicious code safely.
>- Adds an additional layer of security
>- Reduces the risk of malware infection via email attachments while maintaining workflow efficiency for employees

### Monitoring
> is crucial for proactive cybersecurity, providing continuous surveillance of systems, networks, and applications.

> Involves detecting, logging, and responding to specific activities or conditions to identify current issues and anticipate future vulnerabilities

> Can flag unusual account activities such as sudden large withdrawals, frequent international transactions, or simultaneous logins from multiple locations

### **Important/homework**























































































































































































































































































































































































































































































































































































































































































































































































































































