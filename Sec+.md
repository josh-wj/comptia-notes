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










































































































































































































































































































































































































































































































































































































































































































































































