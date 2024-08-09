# Security Fundamentals

## CIA Triad

- **Confidentiality**

  - Ensure measures are taken to prevent sensitive information form being disclosed to unauthorized individuals, entities, or processes.
    - Access Control
      - Passwords, biometric verification, access cards
      - Limit resource access to authorized personal
    - Encryption
      - Encrypting data
    - Secure Communications
      - SSL/TLS for data transmission
  
- **Integrity**
  - Protecting data from unauthorized changes
  - Ensures accuracy and trustworthiness of data
  - Data accuracy, consistency and trustworthiness
    - Access Controls
    - Digital signatures
    - Hash functions
  
- **Availability**
  
  - Ensure that data, systems, and services are accessible to authorized users when they need them
  - Prevent service disruptions due to service failures, infrastructure, malicious attacks or DDoS attacks
  - Fault tolerance
    - Systems than can still operate even if some components fail
  - Backups
    - Regularly backup data
  
## DAD Triad

- Opposite of the CIA triad
- Threat actors

- **Disclosure**
  - Breach of confidentiality
  - Allowing unauthorized access and exposure of information
  
- **Alteration**
  - Loss of data integrity
  - Unauthorized changes are made to data
  
- **Denial**
  - Direct attack on availability
  - Attacks that will take systems offline

## Zero Trust

- Organizations should not automatically trust anything inside or outside their perimeters
- Verify everything trying to connect or access an organization's systems
- Zero trust includes
  - Identity Verification
  - Least privilege access
  - MFA
  - Log and monitor traffic

- Data Plane
  - Implicit Trust Zones
    - Areas where trust is assumed by default
  - Subject/System
    - Entities requesting or granting access
  - Policy Enforcement Point
    - Enabling, monitoring, and terminating connections between subject and enterprise resources
  
- Control Plane
  - Adaptive Identity
    - Dynamically adjusting user/system identity verification based on context
  - Policy driven access control
    - Access granted based on policies, not static permissions
  - Policy Administrator
    - Manages communication path between subject and resources (establish and shut down comm paths)
  - Policy Engine
    - Ultimately responsible for granting access to resources
  - Threat Scope Reduction
    - Minimize attack surface

## Non-Repudiation

- The inability to deny responsibility or obligations
- Implemented using digital signatures

## Authentication

- Verify the identity of the user or device
- Prerequisite to granting access to a system resources

## Authorization

- Occurs after authentication
- Determines what the user is able to do 
- Matches user credentials against access control list (ACL)
  - Permissions define what access are permitted (read, write, execute, delete, modify)
  - Access control
    - Access Control Lists
    - Mandatory Access Control
    - Discretionary Access Control

## Accounting

- Keeping track of activities
- Logging and monitoring of user activities
  - Login times
  - Session duration
  - Accessed resources
  - Network resources used
  - System changes
  - Data transferred

## Accountability

- Ensures individuals or entities are held responsible for their actions within a system

## Gap Analysis

- Used to compare current security posture with a set of standards, best practices or regulatory requirements
- Identify areas for approvement
  - Identification of current state
    - Map out existing security measures, policies, and controls
    - Determination of target state
      - Typically defined by industry standards, regulatory requirements or internal security initiatives
    - Gap analysis
      - Determine difference between current state and target state

