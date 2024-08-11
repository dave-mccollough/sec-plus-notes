# Vulnerabilities

- Weakness in a system that can be exploited by a threat actor to gain access or execute unauthorized actions.

- **Memory Injection**
  - Inserting malicious code into a computers memory
  - Injecting code or scripts into running processes
  - Examples include:
    - Code injection
    - Buffer overflows
      - Data that is meant to be stored in a buffer, exceeds the buffers storage resulting in adjacent memory locations being overwritten
      - Usually detected during vulnerability scans
      - Check length of data before writing to a buffer
      - [Example](https://www.imperva.com/learn/application-security/buffer-overflow/)
    - DLL Injections
  - Can be fixed by secure coding practices - input validation

- **Race Conditions**
  - Vulnerability that occurs when timing of actions affect system outcome
  - System attempts to perform two or more operations at the same time, but operations must be done in the proper order

- **Malicious updates**
  - Threat actor attempts to install a fake update to an OS that weakens the OS security
  - Can be fixed by using code signing

- **OS Based Vulnerabilities**
  - Weakness in the OS that can be used to gain unauthorized access, elevate privileges, etc.
  - Usually resolved by keeping software updated
  - Avoid using OSs that are no longer supported (Windows XP)

- **SQL Injections**
  - Attackers insert malicious SQL code into text fields to run unauthorized SQL queries
  - Resolved by using input validation
  
- **Cross-Site Scripting (XSS)**
  - Typically found in web applications
  - Enables attackers to inject client side scripts into webpages viewed by other users
  - Web application includes unvalidated or unencoded user input as output on a page
  - Resolved by using input validation

- **Hardware Vulnerabilities**
  - Firmware Vulnerabilities
    - Vulnerabilities in low level software that runs on device
  - End of life hardware
    - Devices no longer supported by manufacturer
    - Results in unpatched vulnerabilities
  - Legacy Hardware
    - Older hardware that may not be compatible with current security requirements
  
- **Virtual Machine Vulnerabilities**
  - VM Escape
    - Attacher runs code that lets them break out of VM and into the host machine
  - Resource Reuse
    - Sensitive data that can remain on system resources and be accessed by other processes

- **Cloud Vulnerabilities**
  - Data Breaches
    - Data stored on cloud servers
  - Identity, credential, and access management
    - Weak authentication processes
    - Poor credential management
    - Inadequate access controls
  - Insecure APIs
    - API's not properly secured can be compromised
  - System Vulnerabilities
  - Account Hijacking
    - Attacker gains access to users cloud account

- **Supply Chain Vulnerabilities**
  - Supply chain includes service providers, hardware providers and software providers
  - Service Provider
    - Deliver various IT services (MSP/MSSP)
    - Service providers are a vector for security breaches
  - Hardware Provider
    - Manufactures and distributors of physical computing devices and components
    - Hardware could be tampered with at any point in the supply chain
  - Software Providers
    - Entities that develop and distribute software
    - Software vulnerabilities that can be exploited by attackers to gain access or disrupt services

- **Cryptographic Vulnerabilities**
  - Weakness within the cryptographic algorithms
    - Some older cryptographic algorithms can be broken with enough computing power
    - Cryptographic key management issues
      - Keys not generated, stored or handled correctly
    - Implementation issues
      - Programming errors - buffer overflows

- **Misconfiguration**
  - Improper setup or configuration of hardware or software
    - Leaving default settings
    - Unnecessary services being enabled
    - Inadequate security controls

- **Mobile Device Vulnerabilities**
  - Weakness allowing attackers to gain access to mobile device or data 
    - Outdated operating systems
    - Unsecured network connections
      - Wifi
      - Bluetooth
    - Physical Access
      - Unlocked or unsecured device
    - System flaws
      - Weakness in operating system or hardware
    - User behavior
      - Password sharing
      - Interacting with phishing links
    - Jailbreaking
      - Removing software restrictions imposed by the operating system
      - Known as Rooting on Android devices
    - Sideloading
      - Installing applications on a device from other source other than the app stores
      - 
- **Zero-day Vulnerabilities**
  - Security flaw that is discovered by an attacker before the software or hardware vendor is aware of it or before they have released a patch
  - Zero day refers to developers having zero days to fix the vulnerability
  