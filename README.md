# README
- This repo contains learning material for PaloAlto Firewall basics
- Start with this README for a general overview of the contents of this repo. 

# Palo Alto Networks Overview
- Palo Alto Networks is a global cybersecurity company that provides advanced security solutions to protect networks, data, and users from cyber threats. They offer a wide range of products and services, including: Firewalls, Cloud Security, Endpoint Security, Threat Intelligence.

## Intro ##
### Three Pillars of the Palo Alto Networks Portfolio
- **Network Security**: Protects networks with firewalls that can prevent threats.
- **Cloud Security**: Secures cloud environments, applications, and data.
- **Endpoint Security**: Protects devices like computers and mobile phones from malware and threats.

### Single-Pass Architecture
A design where the firewall processes all network traffic only once to inspect and secure it. This makes it faster and more efficient than processing the same traffic multiple times.

### Zero Trust Concept
This approach assumes no one, whether inside or outside the network, should be trusted by default. Every user or device must verify their identity before accessing any resource.

### Physical and Virtual Firewall Models
- **Physical Firewalls**: Hardware devices that protect your network from threats.
- **Virtual Firewalls**: Software-based firewalls that protect cloud environments or virtualized networks. They work like physical firewalls but on virtual machines.


# Palo Alto Fundamentals: Essential Knowledge for a Security Engineer

As a new security engineer learning about Palo Alto Networks firewalls, understanding the fundamentals is crucial. Here’s everything you need to know:

---

## 1. Introduction to Palo Alto Networks Firewalls
- **Next-Generation Firewalls (NGFWs)** provide deep packet inspection, application-based controls, and advanced threat prevention.
- Unlike traditional firewalls that rely on port-based filtering, Palo Alto NGFWs use **App-ID, User-ID, and Content-ID** for security enforcement.

---

## 2. Palo Alto Firewall Architecture
- **Single-Pass Parallel Processing (SP3):** Ensures high-speed packet processing with reduced latency.
- **Control Plane vs. Data Plane:**
  - **Control Plane:** Handles management functions (configuration, logging, updates).
  - **Data Plane:** Handles traffic processing, packet forwarding, and security inspection.

---

## 3. Initial Setup & Basic Configuration
- **Accessing the Firewall:**
  - Web GUI (`https://<firewall-ip>`)
  - CLI (via SSH or console)
- **Basic Setup:**
  - Configure **management interface** (IP, gateway, DNS, NTP).
  - Change **default admin password** for security.
  - Enable licensing and apply **content updates**.

---

## 4. Interface Types & Networking
- **Interface Types:**
  - **Layer 3:** Firewall acts as a router.
  - **Layer 2:** Firewall acts as a switch.
  - **Virtual Wire (VWire):** Transparent inline mode.
  - **Tap Mode:** Passive monitoring for visibility.
- **Zones & VLANs:**
  - **Security zones** segment traffic and define policies.
  - **VLANs** enable segmentation within the same network.
- **Routing:**
  - Static Routes
  - Dynamic Routing (OSPF, BGP, RIP)
- **Network Address Translation (NAT):**
  - **Source NAT (SNAT)** – Used for outbound traffic.
  - **Destination NAT (DNAT)** – Used for inbound access.

---

## 5. Security Policies & Rule Management
- **Security Policies:**
  - Define rules based on **App-ID, User-ID, and Content-ID**.
  - Default rule: **Implicit deny all** (must create allow rules explicitly).
- **App-ID:** Identifies applications regardless of port/protocol.
- **User-ID:** Integrates with **Active Directory (AD)** for user-based policies.
- **Decryption Policies:** Enable SSL/TLS decryption to inspect encrypted traffic.
- **Security Profiles:** Attach profiles to rules for additional protection:
  - **Antivirus**
  - **Anti-Spyware**
  - **Vulnerability Protection**
  - **URL Filtering**
  - **File Blocking**
  - **WildFire (Sandboxing)**

---

## 6. Threat Prevention & Advanced Security
- **WildFire:** Cloud-based sandbox that analyzes unknown threats.
- **Zone Protection & DoS Protection:** Prevents network flood attacks.
- **File Blocking & Data Filtering:** Prevents unauthorized data exfiltration.

---

## 7. Logging, Monitoring & Troubleshooting
- **Log Types:**
  - **Traffic Logs:** Show allowed/denied connections.
  - **Threat Logs:** Show detected threats and prevented attacks.
  - **System Logs:** Record system activities and admin changes.
- **Monitoring Tools:**
  - Dashboard & ACC (Application Command Center)
  - CLI commands for troubleshooting:
    ```bash
    show system info
    show session all
    show log traffic
    tail follow yes mp-log ms.log
    ```
- **Packet Captures (PCAP):** Used for deep traffic analysis.

---

## 8. High Availability (HA) & Redundancy
- **Active/Passive HA:** One firewall is active, and the other is standby.
- **Active/Active HA:** Both firewalls share traffic.
- **HA Sync:** Ensures consistent policy and session states between devices.

---

## 9. Centralized Management with Panorama
- **Panorama** provides a **single console** to manage multiple firewalls.
- **Benefits:**
  - Push configurations to multiple devices.
  - Collect logs centrally for correlation and analysis.

---

## 10. Automation & API Integration
- Palo Alto NGFWs support automation via:
  - **REST API**
  - **Ansible**
  - **Terraform**
  - **Python SDK (Pan-OS SDK)**
- Automation is useful for **policy management, log analysis, and threat response**.

---

## 11. Palo Alto Certifications & Learning Path
- **PCCSA (Associate):** Entry-level cybersecurity fundamentals.
- **PCNSA (Administrator):** Network security administration (recommended for beginners).
- **PCNSE (Engineer):** Advanced-level Palo Alto firewall management.

---

## Next Steps
1. **Set up a Palo Alto lab** (VM-Series or physical device).
2. **Practice security policy creation, NAT, and threat prevention.**
3. **Learn CLI commands and troubleshoot logs effectively.**
4. **Study for PCNSA certification** to deepen your understanding.

