📘 Flow Control in Computer Networks
🔹 What is Flow Control?

Flow control is a technique used in the Data Link Layer to ensure that the sender does not overwhelm the receiver by sending data faster than it can be processed.
It helps maintain a proper balance between sender and receiver speed.

🔹 Why Do We Need Flow Control?

The sender’s transmission speed is usually faster than the receiver’s processing speed.

Without flow control:

The receiver’s buffer may overflow.

Data loss and retransmission will occur.

Flow control makes sure that the sender adjusts its speed according to the receiver’s capacity.

🔹 Flow Control Techniques
1. Stop-and-Wait Protocol

The sender sends one frame and then waits for an acknowledgement (ACK).

Only after receiving the ACK, it sends the next frame.

Pros: Simple, easy to implement.

Cons: Low efficiency because of waiting time.

2. Sliding Window Protocol

Allows the sender to send multiple frames before needing an acknowledgement.

(a) Go-Back-N ARQ

The sender can transmit multiple frames continuously.

If an error occurs, the receiver discards that frame and all frames after it.

The sender has to resend from the erroneous frame onwards.

Pros: Better utilization of the channel.

Cons: Redundant retransmission.

(b) Selective Repeat ARQ

The sender only retransmits the specific frames that were lost or corrupted.

Pros: More efficient, less retransmission.

Cons: Complex implementation, requires more memory.

🔹 Summary Table
Technique	Working Style	Pros	Cons
Stop-and-Wait	Send 1 frame → Wait for ACK	Simple to implement	Low efficiency
Go-Back-N	Resend from error frame onwards	Better utilization	Redundant retransmission
Selective Repeat	Resend only erroneous frames	High efficiency	Complex, requires more memory
🔹 Real-Life Analogy

Stop-and-Wait: You say one sentence to a friend and wait until they reply "OK" before saying the next one.

Go-Back-N: You say 5 sentences at once. If they didn’t hear the 3rd, you have to repeat from the 3rd sentence onward.

Selective Repeat: If they only missed the 3rd sentence, you just repeat that one.

📌 Conclusion

Flow control ensures smooth, reliable, and efficient communication between sender and receiver.
It prevents data loss, buffer overflow, and synchronization issues in computer networks.
