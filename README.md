# INTERNSHIP-TASK-4-ELEVATORY-LABS
# Windows Firewall Inbound Rules Test

A practical demonstration of Windows Firewall configuration for network security management, focusing on blocking insecure protocols while maintaining secure remote access capabilities.

## 🎯 Project Objective

This project demonstrates the implementation and testing of Windows Firewall inbound rules to manage network traffic effectively. The primary focus is on blocking Telnet (port 23) connections while allowing secure alternatives like SSH, and validating the configuration using PowerShell testing tools.

## 📋 Table of Contents

- [Overview](#overview)
- [Technologies Used](#technologies-used)
- [Key Concepts](#key-concepts)
- [Implementation](#implementation)
- [Testing Results](#testing-results)
- [Security Analysis](#security-analysis)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Conclusions](#conclusions)

## 🔍 Overview

Network security is crucial in modern computing environments. This project showcases how Windows Firewall inbound rules can be strategically configured to:

- **Block insecure protocols** (Telnet on port 23)
- **Allow secure connections** (SSH on port 22)
- **Validate firewall effectiveness** using PowerShell commands
- **Enhance overall system security** through proper traffic management

## 🛠 Technologies Used

- **Windows Firewall with Advanced Security**
- **PowerShell** - Network testing and validation
- **Telnet Protocol** - Target for blocking demonstration
- **SSH Protocol** - Secure alternative implementation
- **TCP/IP Networking** - Underlying communication protocols

## 📚 Key Concepts

### Telnet Protocol
- Network protocol for remote computer access over TCP/IP
- Creates virtual terminal connections for text-based interactions
- **Security Risk**: Transmits data in plain text
- Common uses: Network device management, service testing, troubleshooting

### PowerShell
- Microsoft's advanced command-line shell and scripting language
- Built on .NET framework for system administration
- Capabilities: Task automation, configuration management, network diagnostics
- Supports both interactive commands (cmdlets) and scripting

### Inbound Firewall Rules
- Control mechanisms for incoming network traffic
- Essential for network security and access control
- Filter and restrict access to internal resources
- Protect against malware and unauthorized access attempts

## 🚀 Implementation

### Methodology

1. **Firewall Configuration**
   - Navigate to Windows Firewall interface
   - Review existing inbound rules
   - Create custom security rules

2. **Custom Rules Created**
   - ✅ **Allow SSH Traffic** (Port 22) - Secure remote access
   - ❌ **Block Telnet Traffic** (Port 23) - Security enhancement
   - Verify enabled/disabled status for each rule

3. **Testing Protocol**
   - Use PowerShell for TCP connectivity testing
   - Test against localhost (127.0.0.1)
   - Document results and validate rule effectiveness

## 📊 Testing Results

### PowerShell Test Command
```powershell
Test-NetConnection -ComputerName 127.0.0.1 -Port 23
```

### Results
- **TCP Connection**: ❌ Failed (`TcpTestSucceeded: False`)
- **Network Path**: ✅ Reachable (`PingSucceeded: True`)
- **Conclusion**: Firewall rule successfully blocking port 23 traffic

The test confirms that while the network path remains accessible, the specific port 23 traffic is effectively blocked by the firewall rule.

## 🔒 Security Analysis

### Benefits Achieved
- **Enhanced Security**: Blocked insecure Telnet protocol prevents plain-text transmission vulnerabilities
- **Selective Access**: Maintained secure remote management capabilities through SSH
- **Verified Protection**: PowerShell testing confirms rule effectiveness
- **Best Practices**: Implementation follows network security standards

### Security Improvements
- Prevents unauthorized access through insecure protocols
- Maintains network functionality while enhancing protection
- Provides audit trail through firewall rule documentation
- Enables quick verification of security configurations

## 🏁 Getting Started

### Prerequisites
- Windows operating system with Firewall enabled
- Administrative privileges for firewall configuration
- PowerShell access for testing
- Basic understanding of network protocols

### Setup Instructions
1. Open Windows Firewall with Advanced Security
2. Navigate to Inbound Rules section
3. Create new custom rules as specified
4. Enable/disable rules according to security requirements
5. Test configuration using PowerShell commands

## 💻 Usage

### Creating Inbound Rules
1. Access Windows Firewall settings
2. Select "Inbound Rules" → "New Rule"
3. Choose "Port" rule type
4. Specify TCP protocol and port number
5. Select "Block the connection" for insecure protocols
6. Apply to all network profiles
7. Name and enable the rule

### Testing Configuration
```powershell
# Test blocked port (should fail)
Test-NetConnection -ComputerName 127.0.0.1 -Port 23

# Test allowed port (should succeed)
Test-NetConnection -ComputerName 127.0.0.1 -Port 22
```

## 🎯 Conclusions

This project successfully demonstrates:

- **Effective Traffic Management**: Windows Firewall inbound rules can selectively control network access
- **Security Enhancement**: Blocking insecure protocols like Telnet significantly improves system security
- **Practical Testing**: PowerShell provides reliable tools for firewall configuration validation
- **Best Practices**: Implementing granular firewall rules supports secure network management

The experiment validates that strategic firewall configuration is essential for maintaining network security while preserving necessary functionality.

## 📄 Project Information

**Internship**: Elevate Labs  
**Author**: Menati Vyshnavi  
**Focus Area**: Network Security & System Administration

---

*This project demonstrates practical network security implementation using Windows built-in security tools and PowerShell testing capabilities.*
