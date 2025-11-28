# INSTRUCTIONS

This folder demonstrates, in a controlled and educational setup, how a Python script can be packaged into a Windows executable and how a simple client–server communication flow behaves across systems.

The purpose of this project is to help understand:

- How Python scripts are converted into `.exe` files
- How communication between two endpoints works in a lab environment
- How tools like Microsoft Defender react to custom-built executables
- How build folders and packaging outputs are generated

---

## Overview

1. Place the Python script on a Windows test machine in a **controlled environment**.

2. Use a Python packaging tool (such as PyInstaller) to convert the script into a standalone executable.  
   This step typically produces multiple output folders and files on the desktop, including:

   - `dist/` — contains the final executable  
   - `build/` — temporary build artifacts  
   - `__pycache__/` — Python cache  
   - `*.spec` — configuration file for the packager  

   Only the **dist** folder contains the final executable.

3. The resulting executable (e.g., `backdoor.exe`) can be examined to observe how Windows handles custom binaries.  
   For example, **Microsoft Defender may or may not flag such executables**, depending on behavior, signatures, and heuristics.  
   This is useful for understanding how defensive tools classify custom, minimal Python-based binaries.

4. On the Linux side (e.g., Kali), a simple Python listener/server script can be run *before* launching the Windows executable.  
   This allows you to observe how the Windows program connects back or communicates within a controlled network environment.

5. When the executable is opened on the Windows machine, the listener should show an incoming connection — demonstrating that client–server communication is functioning.

6. This experiment can be used to study:

   - How custom executables interact with the OS  
   - How network listeners detect inbound connections  
   - How endpoint security tools like Microsoft Defender analyse non‑malicious test binaries  
   - Basic concepts of remote communication and monitoring in lab conditions

---

## ⚠️ Important Note

This project is strictly for **educational, research, and authorized testing in controlled environments**.  
It is **not** intended for malicious use.  
Use these concepts only on systems you own or have explicit permission to test.
