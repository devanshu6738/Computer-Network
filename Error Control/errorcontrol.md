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

## 📊 Summary Table

| Technique            | Type             | Key Point |
|----------------------|------------------|-----------|
| Parity Check         | Error Detection  | Detects single-bit errors only |
| Checksum             | Error Detection  | Adds up data units for verification |
| CRC                  | Error Detection  | Polynomial-based, very accurate |
---

## ✅ Key Point
Error control ensures that **complete, correct, and reliable data** is received, even in the presence of transmission errors.

---
