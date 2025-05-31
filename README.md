# Tunnel_madness_CTF_Challenges_HTB
# Tunnel Madness - Hack The Box CTF Challenge

**Tunnel Madness** is a reverse engineering and exploitation-focused Capture The Flag (CTF) challenge on [Hack The Box](https://www.hackthebox.com/), where the goal is to analyze a compiled binary and extract the hidden flag. This challenge emphasizes binary analysis, memory inspection, and brute-forcing techniques.

## 🧠 Challenge Overview

- **Platform:** Hack The Box
- **Challenge Name:** Tunnel Madness
- **Category:** Reversing / Exploitation
- **Difficulty:** Intermediate
- **Main Skills:** Binary Analysis, GDB Debugging, Brute Force

## 🛠️ Tools Used

- **Ghidra** – for reverse engineering the binary and understanding its logic
- **strings** – for inspecting printable strings in the binary
- **file** – to identify the binary architecture and format
- **gdb** – for runtime analysis and memory inspection
- **Python Script** – for brute-forcing password/key (if applicable)

## 🧭 Walkthrough Summary

1. **Binary Inspection**
   - Used `file` and `checksec` to determine binary protections and type
   - Ran `strings` to locate any suspicious output or embedded hints

2. **Reverse Engineering**
   - Loaded the binary into **Ghidra** to analyze the program logic
   - Identified key functions, comparisons, and conditions for success
   - Located hidden function paths and flag-checking logic

3. **Debugging & Runtime Analysis**
   - Used `gdb` to set breakpoints and monitor registers/stack
   - Analyzed buffer lengths and stack behavior to understand validation flow

4. **Brute Forcing**
   - Created a script to brute force correct input byte-by-byte based on output
   - Adjusted based on Ghidra-discovered comparison routines or jump tables

5. **Flag Extraction**
   - Upon successful execution path, captured the flag from program output or memory
🔐 Flag

> `HTB{example_fake_flag_for_display}`  
*The actual flag has been excluded for ethical reasons.*

## 📌 Notes

- This challenge does **not** require any networking or web-based exploitation.
- Purely local binary analysis and exploitation.
- Remember: always participate in CTFs ethically.
