# Sophos EDR & XDR Practical

## Overview

This practical focuses on understanding Endpoint Detection and Response (EDR) and Extended Detection and Response (XDR), followed by implementing and configuring Sophos EDR using Sophos Central.

The practical includes creating a Sophos Central account, installing the EDR agent, creating endpoint security policies, assigning policies to an endpoint, and testing the configured security controls.

---

## 1. Endpoint Detection and Response (EDR)

EDR continuously monitors endpoint devices such as desktops, laptops, and servers to detect, investigate, and respond to security threats.

### Main Features

- Continuous endpoint monitoring
- Real-time threat detection
- Malware and ransomware protection
- Behavioral analysis
- Incident investigation and forensics
- Endpoint isolation and containment
- Automated response and remediation

### Example

If ransomware starts encrypting files on an endpoint, an EDR solution can detect the suspicious behavior, block the activity, isolate the endpoint, and provide information for further investigation.

---

## 2. Extended Detection and Response (XDR)

XDR extends the visibility of EDR by collecting and correlating security information from multiple sources such as endpoints, networks, email, cloud services, identity systems, and servers.

### Main Features

- Centralized threat detection
- Correlation of security events from multiple sources
- Real-time monitoring
- Automated investigation and response
- Behavioral and security analytics
- Broader visibility across the environment
- Faster investigation and remediation

### Example

A phishing attack may begin with a malicious email, followed by account compromise, suspicious endpoint activity, and access to cloud resources. XDR can correlate these events to provide a broader view of the incident.

---

# 3. Sophos Central Account Creation

Sophos Central was used to manage the endpoint security environment.

### Steps Performed

1. Opened Sophos Central in a web browser.
2. Created a Sophos Central account.
3. Entered the required account details.
4. Verified the email address.
5. Logged in to the Sophos Central dashboard.
6. Enabled Multi-Factor Authentication (MFA).

The screenshots in this folder document the account creation and dashboard setup process.

---

# 4. Downloading the Sophos EDR Agent

The Sophos endpoint installer was downloaded from Sophos Central.

### Steps Performed

1. Opened **My Products**.
2. Selected **Endpoints**.
3. Opened the **Installer** section.
4. Selected **Complete Windows Installer**.
5. Downloaded the installer.

---

# 5. Installing the EDR Agent

The downloaded installer was used to install the Sophos endpoint protection agent on the Windows system.

### Steps Performed

1. Ran the installer as Administrator.
2. Accepted the license agreement.
3. Allowed the installer to download the required components.
4. Completed the installation.
5. Restarted the system if required.
6. Opened Sophos Central and checked the endpoint status.

After installation, the endpoint was visible in **Devices → Computers** and its protection status could be verified.

---

# 6. Threat Protection Policy

A custom Threat Protection policy was created to provide protection against malware, ransomware, exploits, and suspicious applications.

### Policy Details

**Policy Name:** `Corporate Threat Protection`

**Description:** Protects endpoints from malware, ransomware, exploits, and suspicious files.

### Configuration

The following security controls were configured:

- Real-time scanning — Enabled
- Scheduled scan — Weekly, Sunday at 2:00 AM
- Potentially Unwanted Applications (PUA) — Enabled
- Ransomware Protection / CryptoGuard — Enabled
- Exploit Prevention — Enabled
- Behavior Monitoring — Enabled
- Automatic Cleanup — Enabled
- Scan USB devices — Enabled
- Scan downloads — Enabled
- Scan archive files — Enabled

After configuring the policy, it was saved and assigned to the protected endpoint.

---

# 7. Threat Protection Policy Assignment

The custom Threat Protection policy was assigned to the endpoint from Sophos Central.

### Verification

After assigning the policy:

1. The endpoint was selected.
2. The assigned policy was checked.
3. The Computers and People section was updated.
4. The endpoint protection status was verified.

The screenshots document the policy configuration and assignment process.

---

# 8. Threat Protection Testing with EICAR

The EICAR anti-malware test file was used to safely test whether Sophos could detect and block a known security test pattern.

### Test Process

1. The official EICAR test file was accessed.
2. The test file was downloaded.
3. Sophos detected the file.
4. The file was blocked or quarantined.
5. A security alert/event was generated in Sophos Central.
6. The endpoint activity was checked from the Sophos Central console.

The EICAR test file is designed for testing antivirus detection and does not contain real malware.

---

# 9. Application Control Policy

A second custom policy was created using Sophos Application Control.

The purpose of Application Control is to restrict unauthorized or potentially risky applications and reduce the attack surface of an endpoint.

### Policy Details

**Policy Name:** `Corporate Application Control`

### Configuration

1. Opened **My Products → Endpoint → Policies**.
2. Selected **Application Control**.
3. Created a new policy.
4. Added the required application or application category.
5. Set the required action to **Block**.
6. Saved the policy.
7. Assigned the policy to the protected endpoint.

---

# 10. Application Control Testing

After assigning the Application Control policy, the configured application restriction was tested on the endpoint.

### Test Process

1. The configured application was launched.
2. Sophos Application Control applied the configured restriction.
3. The application was blocked or restricted according to the policy.
4. The corresponding event was checked in Sophos Central.

This demonstrated how Application Control can be used to restrict selected applications on managed endpoints.

---

# 11. Key Learning

Through this practical, I learned:

- The basic concept and purpose of EDR.
- How XDR provides visibility across multiple security sources.
- How Sophos Central is used for endpoint security management.
- How to install and verify an endpoint security agent.
- How to create and configure a custom Threat Protection policy.
- How to assign security policies to endpoints.
- How to test antivirus detection using the EICAR test file.
- How Application Control can restrict selected applications.
- How centralized security management helps monitor endpoint security events.

---

# 12. Screenshots

The `screenshots` folder contains the screenshots captured during the practical, covering:

- Sophos Central account creation
- Sophos Central dashboard
- EDR agent download
- EDR agent installation
- Endpoint verification
- Threat Protection policy creation
- Threat Protection configuration
- Policy assignment
- EICAR detection/testing
- Application Control policy creation
- Application Control configuration
- Policy assignment and verification
- Application Control testing

---

## Educational Use Notice

This practical was performed for **cybersecurity learning and educational purposes** in a controlled environment.

Security tools and test files should only be used on systems and applications that you own or have explicit permission to test.