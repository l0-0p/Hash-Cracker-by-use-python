# Cryptographic Password Hash Cracker

A localized dictionary attack tool designed to recover plain-text credentials from MD5 hashes. This project explores cryptographic verification mechanisms and highlights the vulnerability of legacy hashing algorithms to pre-computed wordlist matching.

---

## Key Features
* Dynamic Path Mapping: Uses advanced path resolving (os.path.abspath(__file__)) to ensure perfect file loading regardless of the execution environment.
* String Trimming & Normalization: Features rigorous line endings and carriage return (\r\n) filtering for flawless hash matching.
* Real-Time Debug Output: Includes optional verbosity to print each evaluated plain-text candidate alongside its generated hex string.

---

## Setup & Usage

1. Prerequisites: Built entirely using native Python modules (hashlib, os, sys). No external libraries needed.
2. Wordlist Requirement: Create a file named passwords.txt in the exact same directory and fill it with your dictionary words (e.g., password123).
3. Execution:
   `bash
   python hash_cracker.py
