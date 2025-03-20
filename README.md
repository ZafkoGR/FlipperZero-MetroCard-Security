# Flipper Zero and Metro Card Security

## Overview
This repository contains the scientific research paper **"Flipper Zero and Metro Card Security: A Theoretical Analysis of Vulnerabilities in Contactless Fare Systems."** The study examines **Flipper Zero's role in cybersecurity red team assessments** and its impact on **metro card system security**. It provides a **cryptographic analysis of legacy and modern transit card technologies** (e.g., MIFARE Classic, DESFire EV3) and evaluates potential attacks such as **RFID cloning, relay attacks, and replay-based fraud**.

## Problem Statement
Metro card fare systems rely on **contactless smartcards** for quick and efficient transactions. However, these systems are vulnerable to:
- **Cloning attacks** on legacy cards using tools like Flipper Zero.
- **Relay attacks** that extend the reach of valid cards, bypassing proximity restrictions.
- **Weak cryptographic implementations** that allow unauthorized access to transit networks.

Despite advancements in transit card security, **vulnerabilities persist due to outdated encryption, implementation flaws, and inadequate authentication measures**.

## Research Scope & Methodology
The research is based on **literature review, cryptographic analysis, and practical attack simulations** using **Flipper Zero, Proxmark3, and NFC-enabled devices**. The methodology includes:
- **Protocol analysis** of metro cards to identify security mechanisms.
- **Cryptographic key testing** for default and weak keys in smartcards.
- **Replay and relay attack feasibility** to assess real-world security risks.
- **Evaluation of countermeasures** such as AES-based authentication and timing-based defenses.

## Security Analysis

### MIFARE Classic (Legacy Systems)
- **Weak 48-bit Crypto-1 cipher**, vulnerable to brute force attacks.
- **Cloning possible within seconds** using Flipper Zero or Proxmark3.
- **Stored-value manipulation** enables free rides and unauthorized access.

### MIFARE DESFire EV1/EV2 (Advanced Systems)
- Uses **3DES or AES-128 encryption** for stronger security.
- **Mutual authentication** prevents cloning but may still be vulnerable to relay attacks.
- **Potential weaknesses in key diversification and implementation errors**.

### MIFARE DESFire EV3 (Latest Generation)
- Implements **Secure Dynamic Messaging** to prevent replay attacks.
- **Transaction Timer** restricts relay-based exploits.
- **Stronger proximity verification** reduces the risk of distance-based fraud.

---

## Key Findings
1. **Flipper Zero is highly effective against legacy metro card systems (MIFARE Classic), allowing easy cloning and replay attacks.**
2. **Modern transit cards (DESFire EV1/EV2/EV3) offer better protection through AES-based authentication and secure messaging.**
3. **Relay attacks remain a feasible threat, especially when proximity verification mechanisms are not enforced.**
4. **Cryptographic best practices, proper key diversification, and real-time fraud detection are critical to securing transit fare systems.**

## Recommendations
- **Immediate deprecation of MIFARE Classic** in favor of AES-based cards.
- **Enhanced relay attack defenses** using strict time-based proximity verification.
- **Stronger cryptographic implementation** in transit card infrastructures.
- **Regular penetration testing** using security tools like Flipper Zero to assess system weaknesses.

---


## Author and Citation
- **Author**: Konstantinos Zafeiropoulos  
- **Affiliation**: University of West Attica & The American College of Greece  
- **Field of Research**: Cybersecurity, RFID Security, Cryptographic Vulnerabilities  
- **Date**: 2025  

For citation:
📌 **Zafeiropoulos, K. (2025). Flipper Zero and Metro Card Security: A Theoretical Analysis of Vulnerabilities in Contactless Fare Systems. University of West Attica.**

---

## Contact and Contributions
This repository is open for contributions. If you would like to suggest improvements, submit a pull request or open an issue.

For any inquiries:
- **Email**: ice20390293@uniwa.gr  
- **LinkedIn**: https://www.linkedin.com/in/konstantinos-zafeiropoulos/ 
- **GitHub Issues**: For reporting bugs or suggesting enhancements  

Transit security must evolve alongside attack techniques. This research provides insight into **real-world vulnerabilities** and aims to enhance **the security of modern fare collection systems**.

