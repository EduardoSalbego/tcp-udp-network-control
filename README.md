# Reliable Data Transport Protocol over UDP

[![Python](https://img.shields.io/badge/Language-Python-blue)](https://www.python.org/)
[![Network-Programming](https://img.shields.io/badge/Field-Networking-orange)](#)

This project implements a custom transport layer protocol that brings **TCP-like reliability and control features** to the **UDP protocol**. Developed as a practical networking challenge, the goal was to simulate and ensure reliable data transfer in potentially lossy or congested network environments.

---

## Key Features

To achieve reliability over a connectionless protocol (UDP), the following mechanisms were implemented:

* **Flow Control:** Ensures the receiver is not overwhelmed by data, managing the transmission rate based on the receiver's capacity.
* **Congestion Control:** Algorithms designed to detect network saturation and adjust the data flow to prevent packet loss.
* **Guaranteed Delivery:** Implemented retransmission logic (ARQ) to ensure that every packet reaches its destination despite network instability.
* **Packet Ordering:** Sequence numbering to ensure that messages are delivered to the application layer in the correct order, regardless of their arrival sequence at the transport layer.

---

## Performance Analysis

A core part of this project involved benchmarking the custom protocol against standard TCP and UDP. We conducted a test transmitting **1,000 messages** to measure latency and overhead.

| Protocol | Characteristics | Performance Result |
| :--- | :--- | :--- |
| **Standard UDP** | Fast, unreliable, no overhead | **~2.4s** |
| **Standard TCP** | Reliable, high overhead, kernel-level | **~4.2s** |
| **Custom Protocol** | Reliable, application-level control | **~5.1s** |

*Detailed results and comparative charts can be found in the project's presentation slides.*

---

## Installation & Usage

1. **Clone the repository:**
   ```bash
   git clone https://github.com/EduardoSalbego/tcp-udp-network-control.git
   cd tcp-udp-network-control
   ```
2. **Run the Server:**
   ```bash
   python server.py
   ```
3. **Run the Client:**
   ```bash
   python client.py
   ```

### Developed by
**Eduardo Salbego** Software Engineering Student | 5th Semester @ UNIPAMPA

**Maria Rocha** Software Engineering Student | 5th Semester @ UNIPAMPA
