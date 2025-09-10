# 🖼️ Framing in Computer Networks

---

## ❓ Problem in Data Transmission
When data is transmitted as a **continuous stream of bits**, the receiver cannot easily identify:
- Where the **message starts**  
- Where the **message ends**

This creates issues like:
- **Loss of synchronization** between sender and receiver  
- **Error handling problems** (difficult to check if full data is received)  

👉 **Solution:** Use **Framing** at the **Data Link Layer**, which divides data into **frames** with clear boundaries.

---

## ⚙️ Methods of Framing

### 1. **Byte Count**
- The **first field** in the frame specifies the number of bytes in that frame.  
- The receiver reads the count and knows how many bytes belong to the frame.  

🔴 **Problem:** If the count field is corrupted, the receiver loses synchronization for all following frames.

---

### 2. **Byte Stuffing (Character Stuffing)**
- Special characters mark the **start** and **end** of a frame.  
  - Example: `DLE STX` → Start of frame, `DLE ETX` → End of frame  
- If the same special character appears in the data, an **extra escape character** is added to avoid confusion.  

✅ **Advantage:** Clear boundaries for frames  
⚠️ **Problem:** Still dependent on character encoding (works on byte-oriented protocols only).

---

### 3. **Bit Stuffing**
- A **special bit pattern** (flag) is used to indicate frame boundaries.  
  - Example: `01111110` (Flag in HDLC protocol)  
- If this bit pattern appears in the data, an **extra 0** is inserted after 5 consecutive 1s.  

✅ **Advantage:** Works at bit-level (independent of character encoding)  
⚠️ **Problem:** Extra bits increase overhead.

---

## 📊 Summary
| Method          | How it Works | Advantage | Disadvantage |
|-----------------|--------------|-----------|--------------|
| Byte Count      | First field indicates frame length | Simple to implement | Synchronization lost if count field corrupted |
| Byte Stuffing   | Special characters mark boundaries | Easy to detect frame limits | Works only for byte-oriented protocols |
| Bit Stuffing    | Special bit pattern + stuffing extra 0s | Works at bit level, more reliable | Adds overhead (extra bits) |

---

## ✅ Key Point
Framing ensures that the **receiver knows whether a complete frame has been received or not**, making communication **reliable and synchronized**.
