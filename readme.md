# Post-Quantum Cryptography & Network Security Portfolio

**Author:** Shek Lun Leung  
**Email:** sheklunleung.qai@proton.me  

## 📖 Overview

This repository serves as a technical portfolio demonstrating advanced concepts in **Post-Quantum Cryptography (PQC)** and **Network Security**. It features a comprehensive implementation of the NIST-selected **ML-KEM (Kyber)** algorithm for quantum-resistant key exchange and a versatile **Network Port Scanner** for security auditing.

These projects showcase proficiency in:
*   **Cryptography:** Implementation and analysis of Lattice-based algorithms (ML-KEM/Kyber), Hybrid Encryption schemes (KEM + AES-GCM).
*   **Security Analysis:** Understanding of quantum threats (Shor's algorithm), secret key encapsulation, and secure communication protocols.
*   **Network Programming:** Socket programming, Nmap integration, and service fingerprinting.
*   **Scientific Writing:** Technical documentation and academic research paper authoring.

---

## 📄 Research Paper

A detailed academic paper describing the design, implementation, and performance analysis of the Post-Quantum Key Exchange system is available here:

👉 [**Post-Quantum Key Exchange: A Practical Implementation and Analysis of ML-KEM (Kyber)**](./Paper/main.pdf)

**Abstract Highlight:** The paper evaluates the performance of the system across standard security levels (ML-KEM-512, 768, 1024), analyzing key sizes, encapsulation/decapsulation latency, and communication overhead, affirming the viability of PQC for practical deployment.

---

## 🛠️ Project 1: Post-Quantum Key Exchange (Kyber Simulation)

A Python-based simulation of a secure communication channel established using the **Kyber (ML-KEM)** Key Encapsulation Mechanism.

### Features
*   **Full KEM Lifecycle:** Simulates Key Generation, Encapsulation, and Decapsulation.
*   **Hybrid Encryption:** Uses the derived shared secret to encrypt messages with **AES-GCM**, demonstrating a practical KEM-DEM architecture.
*   **NIST Security Levels:** Supports all three official parameters:
    *   `ML-KEM-512` (AES-128 equivalent)
    *   `ML-KEM-768` (AES-192 equivalent - **Recommended**)
    *   `ML-KEM-1024` (AES-256 equivalent)
*   **Performance Benchmarking:** Measures and reports key sizes (pk, sk, ct) and operation execution times (ms).

### Quick Start
Prerequisites: `pip install kyber-py cryptography`

```bash
python script/secure_chat_prototype.py
```

---

## 🛡️ Project 2: Network Port Scanner

A dual-mode network scanning tool tailored for both quick reconnaissance and deep inspection.

### Features
*   **Basic Mode:** Lightweight, fast TCP connect scanner using Python's native `socket` library.
*   **Advanced Mode:** Integrates with **Nmap** (`python-nmap`) for service version detection and OS fingerprinting.
*   **Educational Context:** Includes a modification dictionary that explains the function and security risks associated with common open ports (21, 22, 80, 443, etc.).

### Quick Start
Prerequisites: `nmap` (system package) and `pip install python-nmap`

```bash
python script/PortScanner.py
```

---

## 📚 References & Resources

*   **Kyber Python Implementation:** [GiacomoPope/kyber-py](https://github.com/GiacomoPope/kyber-py)
*   **NIST PQC Standardization:** [PQ-Crystals / Kyber](https://pq-crystals.org/kyber/)
*   **Cryptography Examples:** [cryptography.io](https://cryptography.io/en/latest/)

---
*Licensed under the MIT License.*
