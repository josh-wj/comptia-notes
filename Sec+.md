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
>- fail open/closed
>- load balancing 
>- 802.1X
>- EAP/PEAP
>- NGFW, TLS inspection
>- VPN L2TP IPSEC
>- SD-WAN
>- SAEC



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
>- regulated data
>- intellectual property
>- data states
>- obsfucation
>- masking
>- data classifications and types

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
platform diversity
testing
on/offsite backups
power managment
uninterruptible power supply ( UPS )



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
   > - should also run random scans

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
> Mobile device management (MDM) is crucial for successful implementation of Bring Your Own Device (BYOD) policies.

> BYOD policies raise legal concerns regarding data ownership, privacy rights, and employee misconduct.

> COPE: Corporate owned personnlly enabled

> CYOP: Choose Your Own Device

> VDI: Virtual Desktop Infrastructure  

> Ensure clear separation of organizational and personal information.

> Ensure ability to remotely wipe a remote device

> Encryption, regular software updates, and password complexity are essential for mitigating mobile device security risks.

### Connection Methods
> Bluetooth
> -  is susceptible to attacks like Bluejacking and Bluesnarfing.

> Bluejacking
> - 

> Bluesnarfing
> -  

> Blue bugging
> -

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
> -  LDAP, Kerberos ( ticket based method ), and 802.1X are authentication methods tailored to various environments.

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

## Chapter 15            

### Topics
>- Acquisition/Procurement Process
>- Assignment/Accounting
>- Monitoring/Asset Tracking 
>- Inventory
>- Enumeration
>- Disposal/Decommissioning 
>- Sanitization
>- Destruction
>- Certification
>- Data Retention

### Acquisition/Procurement Process
> Acquiring hardware, software, and data assets in accordance with standards for security and compliance

> Requires collaboration across departments  

> Elements of a procurement review
>- Vendor assessment
>- Product security standards
>- Product licensing and support
>- Cost to keep the asset secure

>- Right to audit clause 

### Third-Party Risk Management (TRPM)
> involves evaluating and managing risks associated with outsourcing services and buying products from third-party vendors. 

> Perform due diligence before choosing third parties.
>- Security policies
>- Track records
>- Compliance with industry standards  

### Assignment/Accounting
> Establishes accountability and responsibility for each asset (hardware, software, or data)

> Ownership
>- Designates individuals or departments responsible for assets from acquisition to decommissioning

> Classification
>- Tags assets according to sensitivity and importance; sets the security level

### Monitoring/Asset Tracking
> Provides ongoing knowledge of asset location, status, and condition

> Inventory:
>- Detailed record of all organizational assets

> Enumeration:
>- A map of inventoried assets’ relationships and dependencies

### Disposal/Decommissioning
> Appropriately disposing of hardware, software, or data assets at the end of their useful tenure

> Assets may contain sensitive information 

> Industries have strict regulations (e.g., HIPAA, SOX) mandating specific disposal procedures

> Electronic waste can be hazardous

### Sanitization
> Removing data from a storage device to prevent recovery, typically by overwriting existing data with random information

> Crucial during decommissioning to ensure no residual data is accessible
> Different levels of sanitization  
>- For highly sensitive data, multiple passes of sanitization may be used in combination with physical destruction

### Destruction
> involves physically disassembling or obliterating hardware assets.

> Shredding
>- Shreds devices into small fragments

> Degaussing
>- Applies a magnetic field to disrupt data

> Incineration 
>- Burns hardware in a controlled environment

> Crushing
>- Uses a hydraulic press to deform the device

> Drilling
>- Drills holes through hard drive platters 

> Acid bath
>- Immerses asset in a corrosive liquid to dissolve parts

### Certification
> Documentation and validation of the disposal and decommissioning process

> Ensures compliance with company policy and relevant laws or regulations

> Certificate of destruction serves as a legally binding document confirming secure and responsible disposal of assets

### Data Retention
> Keeping specific types of information for a designated period

> Mandated by company policy or regulations

> Data must remain secure and accessible only to authorized personnel during the retention period.

> Upon expiration of the retention period, files should be sanitized or destroyed according to company and legal guidelines

### Iportant/Homework
>- Due Care

## Chapter 16

### Topics 

>- Identification Methods
>- Analysis
>- Vulnerability Response and Remediation
>- Validation of Remediation

### Identification Methods
> help locate, identify, and document security flaws in an organization’s digital ecosystem.

> Key identification methods
> - vulnerability scans
> - software composition analysis

### Vulnerability scan tools
> Static Application Security Testing (SAST)
>- Analyze source code or binaries without executing the program

> Dynamic Application Security Testing (DAST)
>- Test applications while running to find vulnerabilities not visible in the code

> I nteractive Application Security Testing (IAST)
>- Combine SAST and DAST for comprehensive analysis

> Threat intelligence platforms (TIPs)
>-  Gather data from various sources to provide threat insights
 
> Security information and event management (SIEM) systems
>- Provide real-time analysis of security alerts generated by network hardware and applications

### Application security
> Identifying and mitigating vulnerabilities in software applications

> Static analysis (SAST) 
>- examines source code or binaries without execution, enabling early identification and resolution of security flaws

> Dynamic analysis (DAST) 
>- tests applications during operation, simulating attacks to uncover vulnerabilities that static analysis might miss

> Package monitoring 
>- continuously surveilles third-party software packages and libraries for security vulnerabilities

### Threat Feeds and Databases
> Threat Feed
>- Real-time repository and transmission channel for data points that indicate cyber threats

> Proprietary/third-party feed
>- Specialized channel of threat feeds, typically requiring subscription

> Open-source intelligence threats (OSINT)
>- Threats shared in public forums, databases, and code repositories

> Information sharing and analysis centers (ISACs)
>- Repositories for organizations to share threats received and learn about others; organized by industry

### Penetration Testing
> Simulates real-world attacks to uncover vulnerabilities in systems, networks, or applications 
>- Planning
>- Reconnaissance
>- Exploitation
>- Post-Exploitation
>- Reporting


### Responsible Disclosure Program
> Framework encouraging ethical reporting of security vulnerabilities

> Outlines secure procedures for external researchers to report discovered vulnerabilities

> Incentives include monetary rewards and public recognition

### Bug bounty program 
> Offers financial incentives for discovering and reporting software vulnerabilities

> Organizations host bug bounty programs to leverage the collective expertise of security researchers  

> Incentives vary from nominal to substantial rewards 

> Ethical hackers often receive public acknowledgment for their contributions, enhancing their reputation and career prospects

### System/Process Audit 
> Comprehensive examination and assessment of an organization's processes, controls, and systems

> May use specialized tools such as Nessus, Wireshark, netflow to examine network traffic and configurations

>Common Tools 


### Analysis
>Transforms raw data about vulnerabilities and threats into comprehensive insights

> Common Vulnerability Scoring System (CVSS)
>- Industry-standard tool for evaluating the severity and urgency of vulnerabilities; assigns scores from zero to 10

> Common Vulnerability Enumeration (CVE)
>- Standardized system for cataloging security flaws; provides historical data about remediation

> Vulnerability Classification
>-  Organized categorization of vulnerabilities based on nature, risk level, affected component, or potential impact

> Exposure factor (EF)
>- Percentage of loss that a company would experience if a specific asset were compromised

> Environmental variables
>- Specific conditions or factors within an organization's context influencing the impact and exploitability of vulnerabilities

> Industry/organizational impact 
>- Potential consequences of vulnerabilities beyond an organization's boundaries

> Risk tolerance
>- Extent to which an organization is willing to accept exposure to threats

### Vulnerability response and remediation
>The systematic process of identifying and addressing vulnerabilities in an organization's technology

> Patching 
>- Applying updates to software components to fix known vulnerabilities

> Segmentation
>- Network segmentation divides a network into smaller segments to contain breaches and minimize damage

> Compensating controls
>- Alternate measures to reduce the risk of existing or potential control weaknesses

> Insurance
>- Provides financial risk transfer in case of data compromise

> Exceptions and exemptions
>- Exceptions and exemptions are granted for vulnerabilities accepted due to business needs or technical constraints

### Validation of remediation
> ensures that vulnerabilities have been adequately addressed.

> Rescanning
>- Running vulnerability scans again after applying patches or making changes

> Audit
>- Involves a thorough manual review, often conducted by an independent third party or internal audit team

> Verification
>- Synthesizes insights from rescanning and auditing activities to affirm the success or failure of remediation efforts

### Reporting 
> turns scanning, patching, verification, and validation into actionable insights.

> Serves as organizational memory for cybersecurity efforts

> Reports vary depending on audience
>- Technical teams
>- Senior management
>- Regulatory bodies
>- Information-sharing organizations

### Important/Homework
static/dynamic analysis

package monitoring
fallse positives/negatives
cvss 1-10 least to most concerning
validation and remediation
## Chapter 17
### Topics
> Monitoring and Computing Resources

> Activities
>- Log Aggregation
>- Alerting
>- Scanning
>- Reporting 
>- Archiving
>- Alert Response and Remediation/Validation

> Tools
>- Security Content Automation Protocol (SCAP)
>- Benchmarks

### Monitoring computing resources
> means continuously overseeing an organization's IT assets to ensure they operate within normal parameters.

> System monitoring
>- Ensures the entire system (servers, devices, and workstations) is vulnerability-free and performing optimally 

> Application monitoring
>-  Ensures software applications are secure, responsive, and optimized for performance

> Infrastructure monitoring
>- Ensures cohesive and secure operation of all technological components within an organization

### Log aggregation 
> involves gathering log data from various sources into a centralized repository for examination.

> A critical process

> Helps turn isolated data points into a coherent narrative

> Log aggregation tools and processes
>- SIEM  
>- syslog-ng (can be added to SIEM)
>- rsyslog (similar to SIEM)

### Alerting
> is the early warning system for security infrastructure.

> Using predefined rules, alerts indicate when immediate attention is required.

> Alert turning refers to setting the alert sensitivity.
>- If too stringent, genuine alerts are likely to be ignored among many false positive
>- If too lax, alerts may not trigger when genuine threats occur

### Scanning
> is a proactive measure for identifying potential weaknesses in systems, applications, and networks.

> Comprehensive; scanning checks for open ports, outdated software, weak email passwords, and more

> Following remediation, scan again to ensure that new vulnerabilities didn’t result from the fix

> Automated scanners
>- Nessus
>- OpenVAS
>- Qualys

### Reporting
> translates technical cybersecurity information for stakeholders.

> Essential for daily decision-making, resource allocation, and strategic planning

> When creating reports, consider your audience (e.g., IT or executives). 

> Technical reports
>- give detailed breakdowns of vulnerabilities, affected systems, and recommended actions for IT.

> Executive reports
>- focus on potential business impacts and make recommendations for strategic risk mitigation.

### Archiving
> is securely storing historical data for long-term retrieval and analysis.

> Digital version of a well-organized filing cabinet
>- Quick access to documents when needed for work and auditing 

> Considerations
>- What data to store
>- Storage duration
>- Data storage security

### Alert Response and Remediation/Validation
> involves validating whether an alert indicates a genuine security threat or a false positive, and then remediating if needed. 

> Quarantining
>- Isolating suspicious files or problematic system activities in a secure environment  

> Alert tuning
>- Continually refining alerts to have a robust and response system

### Security Content Automation Protocol (SCAP)
> is a standardized solution for security automation. It helps implement best practices. For example, it ensures that patches have been applied. 

> SCAP Specifications
>- Languages: OVAL, XCCDF, OCIL, AI, ARF
>- Enumerations: CVE, CPE, CCE
>- Metrics: CVSS, CCSS

### Benchmarks
> are standard points of reference for assessing a system’s security level. Referring to such guidelines can be helpful with:
>- Setting a baseline security posture  
>- Maintaining consistency across an organization’s systems
>- Identifying and tracking measurements for improvement
>- Making security comparisons with industry peers and competitors

### Agents/Agentless
> Agent-Based Solution
>- Software agent is installed on each monitored system
>- Sends data to a centralized management system
>- Offers in-depth data and control, but may use extensive resources and be complex to deploy 

> Agentless Solution
>- Monitors and manages systems without requiring software agents on each system
>- Uses existing protocols for remote tasks
>- Simple to implement and has a light footprint
>- Provides less insight and control 

### Security Information and Event Management (SIEM)
> An SIEM system is a specialized device or software for security monitoring. It collects, correlates, and analyzes logs from multiple systems.

> SIEM functions
>- Log collection
>- Log normalization
>- Log aggregation
>- Log correlation
>- Reporting

### NetFlow
> is a protocol that collects and monitors network traffic data.

> Provides various traffic insights
>- Source
>- Destination
>- Volume 
>- Paths

> Essential for traffic profiling and anomaly detection

### Antivirus software
> prevents, detects, and removes malware.

> Also known as anti-malware

> Viruses and Trojans can damage networks and are costly to overcome; ransomware alone has cost victims billions of dollars.

> Every endpoint device, including workstations, tablets, and phones, should have antivirus software to ensure comprehensive protection

### Data loss prevention (DLP)
> is a comprehensive data protection strategy that uses tools to detect potential data breaches and prevent exfiltration.

> Monitors, detects, and blocks data in use, in motion, and at rest

> Enforces policies defined by regulatory bodies
>- HIPPA
>- PCI DCS
>- GDPR

### Simple Network Management Protocol (SNMP) Traps
> SNMPv3 is a popular protocol for managing and monitoring networks. SNMP traps are alerts sent from SNMP-enabled devices when they have status changes. This facilitates speedy response. 

> Optional SNMPv3 features
>- Authentication: Verifies the legitimacy of trap sources, preventing unauthorized devices from sending false alerts
>- Encryption: Offers encryption to maintain the confidentiality of trap content

### Vulnerability scanners
> automate the identification of weaknesses in systems and networks.

> Work as digital sentries by constantly monitoring  

> Stages of vulnerability scanning
>- Pre-assessment
>- Scanning
>- Post-scan analysis
>- Remediation and verification
>- Continuous monitoring

### Important/Homework
>- log aggregattion 
>- scap
>- first 3 charachteristics of dlp
>- snmp trap

## Chapter 18
### Topics
>- Firewall
>- IDS/IPS
>- Web Filter
>- Operating System Security
>- Implementation of Secure Protocols
>- DNS Filtering
>- Email Security
>- File Integrity Monitoring
>- DLP
>- Network Access Control (NAC)
>- Endpoint Detection and Response (EDR)/Extended Detection and Response (XDR)
>- User Behavior Analytics

### firewall
> is a network security device or software that monitors incoming and outgoing network traffic.

> Firewall rules control the flow of data packets.

> Access control lists (ACLs) govern how traffic flows through the network.

> Ports are virtual docks where network services can receive data.

> Protocols are rules and conventions governing data transmission and acceptance.

> A screened subnet is a segment that separates the internal network from an external network (e.g., the Internet).

### IDS/IPS
> Intrusion detection systems (IDSs)
>- monitor and issue alerts about suspicious activities.

> Intrusion protection systems (IPSs)
>- are proactive; they block known or potential threats.

> These systems use predefined signatures (such as specific strings of data) to identify threats. However, known signatures could become irrelevant as new variants of malware emerge.
> Trends identified in analyses of logs can indicate the presence of new vulnerabilities.

### Web filter
> controls access to websites or specific web content based on predefined criteria.

> Agent-based web filtering
>- deploys software directly onto individual user devices. 

> A centralized proxy
>- can serve as an intermediary between user devices and the Internet.

> Reputation-based filtering
>- blocks or allows websites based on their histories

### Operating system security 
> is the first line of defense against unauthorized access and malicious attacks.

> A group policy
>- is created by system administrators to establish detailed rules (policies) for OS and application behavior. 

> SELinux (Security-Enhanced Linux) 
>- uses mandatory access controls to restrict the actions of users and system processes

### implementation of secure protocols 
> refers to creating encrypted pathways for communication.

> Protocol selection:
>- Choosing the appropriate communication standard for data exchange (e.g., HTTPS)

> Port selection:
>- Choosing specific entry and exit points (ports) in the network for data  

> Transport method selection:
>- Choosing a method of securely transporting data packets across the network

### DNS filtering
> is the practice of blocking access to specific websites, web pages, or IP addresses.

> Crucial for preventing access to malicious or inappropriate sites

> Users might attempt to bypass with VPNs or other methods

### Email security
> involves measures used to secure the access and content of email accounts or services.

> Domain-Based Message Authentication, Reporting and Conformance (DMARC)
>- helps receivers verify the authenticity of emails from specific domains 

> DMARC process
>- SPF check
>- DKIM check
>- DMARC policy retrieval
>- Policy enforcement
>- Reporting

### File integrity monitoring 
> involves the regular checking of files for changes or alterations.

> Alerts administrators to the unauthorized access or modification of files

> False positives are a challenge; many authorized changes could be flagged as suspicious

### Data Loss Prevention(DLP)
> is a comprehensive approach to preventing users from sending sensitive or critical information outside the corporate network.

> Describes software products that let network administrators control data access and transfer

> Alerts administrators to unauthorized data transfer attempts

> Aids in incident response

### Network Access Control (NAC)
> is a method to enforce policy-driven security solutions at the network entry level.

> Checks if devices comply with predefined security rules before granting access to the network

> Drawbacks
>- Adds complexity to network administration  
>- Can be circumvented, compromising network security

### Endpoint Detection and Response (EDR)/ Extended Detection and Response (XDR)

> (EDR) systems
>- Monitor endpoints such as desktop computers, laptops, and mobile devices
>- Detect and respond to signs of malicious activities

> (XDR) systems
>- Take a holistic view of network security, correlating data across various channels and layers like email, cloud, and network traffic
>- Identify complex, multi-stage attacks that may evade EDR systems

### User behavior analytics 
> use machine learning algorithms to track, collect, and assess user behavior on a network.

> Analytics help IT detect unusual activity that could indicate security threats, such as sudden changes in file access patterns.

> Alert tuning is important to avoid excessive false positives

### Important/homework


## Chapter 19
### Topics
>- Provisioning/De-provisioning User Accounts 
>- Permission Assignments and Implications
>- Identity Proofing
>- Federation
>- Single Sign-On (SSO)
>- Interoperability
>- Attestation
>- Access Controls
>- Multifactor Authentication (MFA)
>- Password Concepts
>- Privileged Access Management Tools

### Provisioning/De-provisioning User Accounts

> Provisioning
>- Setting up a user account with necessary permissions and access settings  

> De-provisioning
>- Disabling or removing permissions and settings from a user account 

> Well-managed provisioning and de-provisioning are crucial for ensuring users always have appropriate access

### Permission Assignments and Implications
> Permission assignment
>- Granting specific levels of access or activities (e.g., read, edit, delete) to users, groups, or system processes  

> Types of permission assignments
>- User-level  
>- Group-level  
>- Role-based  
>- Resource-based

### Identity proofing 
> is the process of verifying a user's or system's identity within an organization.

> Involves multiple levels of authentication ranging from passwords to biometric data

> Extends beyond initial authentication; includes periodic re-authentication or session time-outs

### Federation
> One system authenticates users and sends their authentication information to other systems.

### Single sign-on 
> enables one set of credentials for access to multiple services or applications.

> Minimizes the number of times a user needs to authenticate after initial login

> SSO protocols
>- LDAP (Lightweight Directory Access Protocol)  
>- OAuth (Open Authorization) <- uses creds ( OpenID runs on top in modern devices ) <- uses tokens
>- SAML (Security Assertion Markup Language)

### Interoperability 
> is the ability of different systems to work together. It’s crucial for identity and access management (IAM) systems. 

> IAM systems need to integrate seamlessly with various databases, applications, and authentication protocols. Lack of integration interferes with needs for access and auditing. 
> Collaboration with external partners requires secure cross-boundary authentication and authorization.
> Interoperable IAM systems can adapt to new technologies and compliance requirements without overhauling existing infrastructure

### Attestation 
> provides evidence or proof, allowing one program or system to authenticate itself to another.

> Remote attestation enables a system to make reliable statements about the software it's running to another system, which can make authorization decisions based on that information.

> A TPM (Trusted Platform Model) quote operation verifies the contents of a TPM chip's platform configuration registers (PCRs) during provisioning.

> Methods of attestation may be vulnerable to replay attacks, masquerading, and other cyberthreats.

### Access controls 
> organize and manage admission to physical areas and computer systems.

> Role-based access control (RBAC)
>- is controlled by the system, not the resource owner. When users are assigned a role, they get access to its resources.

> Rule-based access control
>-  is also known as label-based access control. Example of a rule governing access: During certain hours each day, access is only permitted to specific IP addresses. 

> Mandatory access control (MAC)
>-  is the strictest control. It’s set by the system and uses security classifications for data

> Discretionary access control (DAC)
>- is generally determined by the owner. 

> Attribute-based access control (ABAC)
>- is dynamic and uses context. It can combine various user, group, and resource attributes to determine whether access should be granted.

> Least privilege
>- means the user only has the access required for their job.

### Multifactor Authentication (MFA) 
> is the process of authenticating a user by validating two or more claims from different categories of factors.

> Two-Factor Authentication (2FA)
>- A subset of MFA in which two factors are required to authenticate

> Factor categories
>- Something you know, password, pin, etc
>- Something you have, smart card, OTP token
>- Something you are, Biometrics                                                          

> **Biometrics** (distinctive body measurements) and **security keys** (hardware devices) may be part of MFA

### Password concepts 
> are guidelines and practices for ensuring strong, secure passwords.

> Passwords serve as the primary barrier to protect sensitive information and access controls.

> Issues to consider when setting password requirements
>- Password length
>- Password complexity
>- Password reuse
>- Password expiration
>- Password age

### Privileged Access Management (PAM) Tools
> centrally manage access to privileged accounts based on the principle of least privilege.

> **Just-in-time (JIT) permissions** give access for a limited period.

> **Ephemeral credentials** are generated for specific sessions or tasks and invalidated shortly after completion. They expire more quickly than JIT permissions. 

> **Password vaulting** means using a centralized, encrypted repository to store various access credentials

### Important/homework


## Chapter 20
### Topics
>- Use Cases of Automation and Scripting
>- Benefits
>- Other Considerations

### Use Cases of Automation and Scripting
> **Automation and scripting are vital** in cybersecurity. 

> Handle repetitive tasks efficiently and effectively

> Support policy compliance by consistently applying rules and configurations

> Examples
>- User provisioning  
>- Resource provisioning
>- Policy enforcement
>- Incident response
>- API integrations

### User provisioning 
> involves setting up user accounts with appropriate permissions and roles.  

> **Manual user provisioning** can be time-consuming and is prone to errors.

> **Automation tools integrated with HR software** can automate user provisioning, ensuring the right access for employees at the right time.

> **Deprovisioning** can also be automated

### Resource provisioning 
> automates the setup, modification, or removal of digital assets such as virtual machines, databases, and storage units.

> **Automated resource provisioning** helps ensure uniformity, compliance, and time savings.

> Avoids the errors associated with manual provisioning

### Guard rails 
> are automated safety measures or rules implemented within a system. 

> Designed to restrict or control activities that could be harmful or noncompliant with security policies

> Act as internal checkpoints or barriers guiding user behavior and system interactions  

> Enforce compliance with data privacy regulations like HIPAA

### security group
> is a group of users who are categorized together based on security policies.

> Access to system resources can be automatically updated or modified.  

> **Security group automation** applies templates based on resource roles or functions instead of configuring firewall rules individually.

> Using security groups helps maintain a consistent security posture

### Ticket Creation and Escalation
> Automation streamlines ticket creation and ticket escalation in incident response scenarios.

> An automated system detects irregularities, such as unauthorized login attempts, and generates tickets or incident reports accordingly.

> In case of escalation, such as multiple unauthorized login attempts, tickets are automatically forwarded to higher levels of expertise or authority.

> Automation lets admins control permissions by enabling or disabling services and access based on specific conditions (e.g., regular work hours) or security incidents

### Continuous Integration and Testing (CI/CT)
> involves the automated integration of code changes contributed by multiple developers into a single repository.

> Key processes  
>- Code commitment
>- Static analysis
>- Automated build process
>- Automated testing
>- Deployment

### Integrations and Application Programming Interfaces (APIs)
> **Integrations and APIs** automate the linking of computing services and software applications to establish coherent systems.

> **APIs** enable different software entities to seamlessly communicate with each other.

> Automation is overall beneficial but requires ongoing maintenance and monitoring for errors

### Benefits of Automation
> Efficiency
>- Accelerates task execution, freeing human resources for other work

> Workforce multiplier
>- Enhances team productivity

> Employee retention
>- Improves job satisfaction and retention rates by removing tedious manual tasks

> Reaction time
>- Facilitates quick response to security incidents or operational events

> Baseline enforcement
>- Ensures consistent application of predefined security settings  

> Standardized infrastructure configurations
>- Maintains uniformity in system setups, reducing misconfigurations

> Secure scaling
>- Helps organizations securely expand their digital infrastructures

### Other Considerations About Automation

> Complexity
>- Automation often requires specialized skills for design, implementation, and maintenance. 

> Cost
>- Automation involves initial investments in software, hardware, and human resources.

> Single points of failure
>- Systems without redundancies and fail-safes can become single points of failure. 

> Ongoing supportability
>- is needed for the effective, long-term operation of automated systems.

> Technical debt may accrue.
> That’s the long-term cost of using outdated systems, shortcuts, and temporary fixes to implement an automation rollout.

### Important/homework
> API's/restful API's
> SOAR ( Security Orchestration, Automation, and Response )

## chapter 21
### Topics
>- Process
>- Training
>- Testing
>- Root Cause Analysis
>- Threat Hunting
>- Digital Forensics

Incident Response Process

>- Preparation
>- Detection and Analysis
>- Containment, Eradication, and Recovery
>- Post-Incident Activity

### Preparation
> creates the plan for responding to and recovering from security incidents. 
>- Designating a plan owner  
>- Tech preparation
>- Training programs

###Detection and analysis
> are accomplished with a mix of automated monitoring and human expertise.

> Early detection is best. An early indicator of compromise (IoC) might be unusual network traffic or multiple failed logins. 

> Analyze the IoC to understand the nature and scope of the threat

### Containment, Eradication, and Recovery
> Containment involves isolating the threat from the rest of the network. 
>- Short-term or long-term

> Eradication involves completely removing the threat.
>- Ensure affected systems are backed up, then reimage  
>- Apply patches and change passwords

> Recovery involves choosing a restoration point and validating the system.
>- Increase monitoring for 30+ days following incident

### Post-incident activity 
> is the “lessons learned” phase of incident response. 
>- Meet within two weeks.
>- Complete documentation about the incident.
>- Discuss the response process.
>- Change the response process if needed.
 
### Training 
> equips teams with the knowledge and protocols for effectively managing security incidents.

> Role-based training for individuals and departments 

> Tabletop exercises and simulations for practice responding

### Testing 
> is the rigorous examination of incident response procedures, plans, and capabilities.

> Ensures effectiveness of cybersecurity incident response

> Identifies gaps in responding; serves as a feedback loop for refinement of response strategies

### Tabletop exercises 
> simulate hypothetical situations that mirror real-world threats.  

> **Each participant plays a role** corresponding to their actual emergency responsibilities.

> **Time pressure** helps simulate the urgency of real incidents.

> **Decision points** pause the action for strategic discussions about how to proceed. 

> **Detailed records** are kept of every action, decision, and discussion point.

### Simulation exercises 
> build upon tabletop exercises with simulated tech environments such as sandboxed or isolated replicas of networks.

> Tips for conducting a simulation
>- Define key **performance indicators (KPIs)** to evaluate response effectiveness.  
>- Introduce unexpected elements (e.g., power outages) to test the team's adaptability.
>- Include a post-exercise discussion to identify gaps and discuss improvements.

### Root cause analysis 
> is critical for identifying the  reasons underlying security incidents.
>- Data collection
>- Timeline analysis
>- Hypothesis development
>- Hypothesis confirmation or rejection

### Threat hunting 
> is a proactive search through networks and data sets to detect and isolate advanced threats.

> Targets threats that evade traditional reactive security measures

> Involves setting a specific type of threat, such as lateral moves or data exfiltration

> Discoveries may lead to threat remediation and updated security measures.

### Digital forensics 
> is a multidisciplinary approach to collecting, analyzing, and preserving data.

> Involves the electronic data relevant to investigations or legal proceedings

> Combines technical expertise with legal frameworks and ethical considerations

### Legal Hold and Chain of Custody

> Legal hold
>- is the process of preserving electronic evidence related to a legal case or investigation. It prevents the alteration or deletion of specific data.

> A chain of custody
>- documents the path that evidence takes from acquisition to disposal.
>- Helps ensure integrity and admissibility of evidence in legal proceedings
>- know first 3 parts 

### Acquisition 
> is the systematic collection of digital evidence meant to maintain its authenticity.  

> Follows the order of volatility; captures the most volatile data first (CPU cache and registers)

> Uses special tools to capture RAM

> Creates a bit-by-bit image of the hard drive

> Captures network traffic and logs

> Looks for suspicious artifacts (residual data) such as changes in system settings

### Reporting 
> is the documenting of activities and findings throughout the forensic process.

> Serves as a record for internal review and may become critical evidence in legal proceedings
> Elements of a well-structured report
>- Timeline of events 
>- Tools used
>- Evidence found
>- Steps taken

### Preservation 
> involves safeguarding evidence from identification to the end of its lifecycle.

> Secure, climate-controlled environment

> Tamper-evident storage

### E-discovery 
> involves identifying, collecting, and producing electronically stored information in response to a legal request.

> Subject to specific rules and protocols

> Uses specialized software for searching, identifying, and collecting electronic information

> Ensures that collected information is relevant and not privileged before production

### Important/homework
>- Lessons Learned


## chapter 22
### Topics
> Log Data
>- Firewall Logs
>- Application Logs
>- Endpoint Logs
>- OS-Specific Security Logs
>- IPS/IDS Logs
>- Network Logs
>- Metadata

> Data Sources
>- Vulnerability Scans
>- Automated Reports
>- Dashboards
>- Packet Captures

### Log data 
> is the systematically recorded information that’s generated by hardware, software, and operating systems.

> Captures events, transactions, and other activities within a system or network

> Serves as a chronological record for troubleshooting, security monitoring, and investigations

> Required by various regulations  (HIPAA, PCI DSS, SOX)

> **Syslog** is a commonly used protocol for centralizing log data.

### Firewall logs 
> help IT monitor the traffic allowed and denied by a firewall.

> Reveal typical traffic patterns and unauthorized access attempts 

> Common elements
>- Timestamp
>- Action (ALLOW or DENY)
>- Protocol (TCP)
>- Source IP
>- Destination IP
>- Source port 
>- Destination port

> E.X
>- 2023-09-23 14:32:10 ALLOW TCP 192.168.1.2 8.8.8.8 443 80

### Application logs 
> are records of services, events, and systems within an application.

> Provide (nearly) end-to-end visibility of activity

> It’s important to parse, partition, and analyze all logs related to security incidents.

> Critical process data logged about the user, application, and system can help responders understand the nature and extent of an attack.

> Shimming ( attack focused on drivers )
> Refactoring completly changes the code of the driver but the functions remain the same ( not nessasasarily an attaack )  

### Endpoint logs 
> give detailed information about activities on individual devices connected to a network.

> Help identify suspicious or unauthorized behaviors
>- Installation of unauthorized software
>- Attempts to access restricted files
>- Unrecognized application executions 

> Examples
>- 2023-09-23 14:35:00 User "JohnDoe" initiated "New_Outbound_ Connection" to IP "203.0.113.42" on Port "8080" 
>- 2023-09-23 14:36:00 User "JohnDoe" executed "Unknown_ Application.exe"

### Operating system (OS)-specific security logs 
> provide information about events and activities on a specific system.

> System processes, driver loading data, errors, warnings, and failures

> In Windows, logs can be obtained via the Event Viewer and Windows Admin Center.

> On Linux hosts, log files are typically found in the /var/log directory.

> Collect system logs regularly and store them in a secure and separate location.

### Intrusion Prevention System (IPS)/ Intrusion Detection System (IDS) Logs
> An IPS and IDS work together to prevent and detect potentially harmful activities within a network. Their logs can alert you to various attacks such as SQL injections and cross-site scripting.

> Generated by solutions like Snort and Suricata

> Examples
>- 2023-09-23 13:45:32 ALERT SQL Injection detected from 192.168.1.4
>- 2023-09-23 13:46:10 ALERT Brute-force attempt from 203.0.113.7

### Network logs 
> capture data traffic across the network infrastructure.

> Generated by network monitoring tools like Wireshark and SolarWinds

> Provide insights into bandwidth usage, connection times, and protocol types

> Examples
>- 2023-09-23 14:20:15 INFO TCP Connection from 192.168.1.2 to 8.8.4.4 
>- 2023-09-23 14:21:00 WARNING Large data transfer to 203.0.113.8

### Metadata 
> is information about data, such as activities performed on personal computers or mobile phones. 

> While individual metadata may seem irrelevant, it becomes valuable when combined with other data 

> Categories of metadata
>- Descriptive  
>- Structural
>- Preservation
>- Use
>- Provenance
>- Administrative

### Data sources 
> in IT are the tools and methods utilized to gather, analyze, and present information for investigations.

> Sources range from vulnerability scans to dashboards with real-time analytics.

> Understanding data sources is critical for a comprehensive approach to cybersecurity.

### Vulnerability scans 
> systematically examine networks, systems, or applications to identify and assess security weaknesses.  

> Specialized software probes for known vulnerabilities

> Network scans should include all devices with IP addresses and their software

> Save results for 24 months+

### Automated reports 
> synthesize various security metrics and events.

> Follow regular schedules (e.g., daily scanning) and can also be triggered by specific events

> Generated by Security Information and Event Management (SIEM) systems like Splunk and IBM QRadar

> Offer insight into potential security threats and anomalies

### Dashboards 
> A dashboard is a user interface that organizes information for easier understanding and real-time monitoring of network performance and security.

> Typically uses graphs, charts, and gauges

> Serves as a centralized display, consolidating data from multiple sources

### Packet captures 
> give a detailed view of network activity.  

> Analysts use packet captures to:
>- Identify suspicious patterns
>- Detect deviations from normal network behavior

> Wireshark is commonly used to capture and analyze packets.

### Important/homework
>- vulns. scans


## Chapter 23
### Topics
>- Guidelines
>- Policies
>- Standards
>- Procedures
>- External Considerations
>- Monitoring and Revision
>- Types of Governance Structures
>- Roles and Responsibilities for Systems and Data

### Guidelines 
> are general recommendations aimed at steering organizational behavior and decision making.

> Provide directional advice; suggestions and best practices for various security-related activities

> More relaxed than policies or standards, allowing for flexibility in implementation























































































































































































































































































































































































































































































































































































































































































































































































































































































