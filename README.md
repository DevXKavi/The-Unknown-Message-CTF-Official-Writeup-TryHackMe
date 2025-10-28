# The Unknown Message — CTF Official Writeup

**Author / THM username:** kave3nirmal141  | Created by ME
Link: https://tryhackme.com/jr/theunknownmessage

---

## Overview
Lumen-9, a deep-space reconnaissance satellite, went silent during a routine pass. The player’s mission is to analyze recovered artifacts (communications, telemetry, blackbox, and an image) to reconstruct the final timeline and reveal the hidden message.

**Files provided in the CTF:**  
`comm.txt`, `telemetry.log`, `blackbox.dd`  

**Goal:** Recover uplink details, reconstruct the stego password from Base64 fragments, find the mission log filename, and extract the final hidden message.

---

## Real-World vs. CTF Adjustments
Satellite systems are far more complex in reality, so a few elements were simplified:

- **Comm logs:** Real RF links and space-packet protocols are shown as readable IP/port logs.
- **Telemetry:** Normally binary and encoded — provided here as plain text.
- **Blackbox data:** Actual spacecraft storage replaced with a standard `.dd` image.
- **Image file:** Used for steganography instead of real mission imaging formats.

These changes keep the investigation realistic in concept while making analysis practical.

---

## Tools Used
`echo`, `rev`, `base64`,
