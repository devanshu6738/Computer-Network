# ⚡ Error Control in Computer Networks

---

## ❓ What is Error Control?
Error control is a function of the **Data Link Layer** and **Transport Layer** that ensures data is delivered **accurately and reliably** from sender to receiver.  

It deals with:
- **Error detection** → Checking if data got corrupted during transmission.  
- **Error correction** → Fixing or retransmitting corrupted data.  

---

## 🎯 Why Error Control?
When data travels across a network, it may get corrupted due to:
- Noise
- Interference
- Signal distortion  

👉 Error control ensures the receiver gets either **correct data** or can **request retransmission**.

---

## 🛠 Methods of Error Control

### 1. **Error Detection**
Used to detect if errors occurred in transmission.  
- **Parity Check** → Adds a parity bit (even/odd)  
- **Checksums** → Sum of data units is sent; receiver compares  
- **Cyclic Redundancy Check (CRC)** → Polynomial-based error detection, more reliable  

---

### 2. **Error Correction**
Used to not only detect but also correct errors.  
- **Automatic Repeat Request (ARQ)** → If error detected, frame is retransmitted.  
  - **Stop-and-Wait ARQ** – Send one frame, wait for ACK/NACK.  
  - **Go-Back-N ARQ** – Multiple frames sent, retransmit from the error frame onwards.  
  - **Selective Repeat ARQ** – Only the erroneous frame is retransmitted.  
- **Forward Error Correction (FEC)** → Extra redundant bits allow receiver to correct errors without retransmission.  

---

## 📊 Summary Table

| Technique            | Type             | Key Point |
|----------------------|------------------|-----------|
| Parity Check         | Error Detection  | Detects single-bit errors only |
| Checksum             | Error Detection  | Adds up data units for verification |
| CRC                  | Error Detection  | Polynomial-based, very accurate |
| Stop-and-Wait ARQ    | Error Correction | Simple, but inefficient |
| Go-Back-N ARQ        | Error Correction | Retransmits from error frame onwards |
| Selective Repeat ARQ | Error Correction | Only retransmits erroneous frame |
| FEC                  | Error Correction | Corrects errors without retransmission |

---

## ✅ Key Point
Error control ensures that **complete, correct, and reliable data** is received, even in the presence of transmission errors.

---
