# Security Principles

- **Infrastructure Considerations**
  - Various apsects of IT infrastructure that need to be secured against cybersecurity threats

- **Device Placement**
  - Strategic positioning of hardware components within IT infrastructure
  - Physical and network locations
  - Environmental factors, redundancy, and scalability
  - Effective device placement is ensuring optimal performance, security and resilience

- **Security Zones**
  - Segments within a network that have distinct levels of security controls
  - Common security zones include 
    - External zones
    - DMZ zones
    - Internal Zones
  - Control access and exposure

- **Attack Surface**
  - Number of points an attacker can try to enter or extract data
  - All exposed areas that are vulnerable to cyber attacks
  - Physical and digital aspects
  - The more complex the system or network, the greater the attack surface

- **Failure Modes**
  - Different manners or conditions in which a system, network, or component can fail to perform it's intended function
  - Hardware or software loss
  - Could lead to security breach or data loss
  - Fail-open
    - If system fails, access or traffic can pass through
  - Fail-closed
    - System defaults to closed state if there is a failure
      - Denies access or stops traffic if a failure is detected

- **Device Attributes**
  - Properties or operational behaviors of network security devices
  - Determines how a device interacts with network traffic

- **Network Appliances and Senors**
  - Devices designed to perform specific functions within a network
  - Typically optimized for 
    - Routing 
    - Switching
    - Security
    - Load balancing 
    - Storage
  - Senors
    - Components that collect or analyze data
    - Identify potential security threats or defects

- **Jump Server**
  - Secure computer that acts as a controlled entry to a server or server group

- **Proxy Server**
  - Intermediary between a users computer and the internet
  - Requests resources on behalf of the user
  - Masks users IP address
  - Content filtering
  - Cache frequently accessed content

- **IDS/IPS**
  - Intrusion Detection System (IDS)
    - Realtime monitoring and analysis of network traffic and data for potential intrusions
    - Monitor and analyze user and system activities
    - Assess integrity of files
    - Pattern recognition of known attacks
    - Advantages
      - Dynamically adapts to new, unique, or original attacks
    - Disadvantages
      - Higher false positives
    - Host Based IDS
      - Monitors host machine on which it was installed
    - Network based IDS
      - Used to monitor and analyze network traffic
  - Intrusion Protection System
    - IPS
      - Network security/threat prevention technology

- **Load Balancer**

- **802.1x and EAP**
  - Port Security
    - Secure ports on computers and network devices
    - Guard against unauthorized access and ensure communication channels
    - Prevents unauthorized access
    - Reduces attack surface
  - 802.1x
    - IEEE standard for port based network access control (PNAC)
    - Used to authenticate devices that are attempting to connect to a WAN or a LAN
    - When a device is connected, blocks all traffic till it is authenticated
  - EAP
    - Extensible Authentication Protocol
      - Supports multiple password mechanisms
        - Passwords
        - Certificates
        - Tokens
        - Public key encryption

- **Firewalls**
  - Monitors and controls incoming and outgoing network traffic based on predetermined security rules
  - Establishes a barrier between a trusted secure network and outside network
  - Implemented by software or hardware
  - Controls the flow of traffic 
  - Firewall Types
    - Packet filtering firewalls
    - Staeful inspection firewalls
    - Web application firewalls
    - Unified threat management
    - Next Generation firewalls
  - Layer 4 Firewall
    - Data transport
  - Layer 7 Firewall
    - Inspect content
    - Make decisions based on the data and application specific behaviors

- **VPN**
  - Virtual Private Network
  - Creates an encrypted connection over a less secure network
  - Built on top of existing physical networks
  - Established by creating a virtual point to point connection
  - Uses
    - Dedicated connections
    - Data encapsulation
    - Virtual tunneling protocols
      - TLS - Transport Layer Security
        - Layer 4
        - Uses TLS/SSL
      - IP Security - IPSec
        - Standalone VPN protocol
        - Provides secure authentication and encryption
        - Performs limited authentication
    - Traffic encryption

- **SD-WAN**
  - Software defined wide area network
  - Provides centralized control to direct traffic across a WAN
  - More efficient data routing, reduced latency and improved network performance
  - 