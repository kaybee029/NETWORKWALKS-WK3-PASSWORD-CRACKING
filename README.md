# NETWORKWALKS-WK3-PASSWORD-CRACKING
Breaking down password security: A comparative lab using John the Ripper and Networkwalks tools to crack password-protected PDFs via dictionary attacks.

# 🔐 Password Cracking Lab: John the Ripper vs. Networkwalks

![CyberSecurity](https://img.shields.io/badge/Focus-CyberSecurity-red)
![EthicalHacking](https://img.shields.io/badge/Topic-EthicalHacking-blue)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📌 Overview
This repository documents a hands-on cybersecurity lab focused on **Password Security and Dictionary Attacks**. The objective was to demonstrate how weak, predictable passwords can be easily compromised when attackers have access to hashed data.

The lab was approached using two distinct methodologies:
1. **Local Tooling:** Using John the Ripper (JTR) with the Johnny GUI on Windows.
2. **Browser-Based Tooling:** Using Networkwalks' custom web utilities (Hash Calculator & Password Cracker).

Both methods successfully extracted a hash from a password-protected PDF and cracked it using a dictionary attack, proving that **weak passwords are a critical vulnerability regardless of the encryption method used.**

---

## 🛠️ Tools Used
- **John the Ripper (JTR) / Johnny GUI:** Industry-standard password cracker.
- **Networkwalks Hash Calculator:** Browser-based tool to extract PDF hashes.
- **Networkwalks Password Cracker:** Browser-based dictionary attack simulator.
- **Target File:** A password-protected PDF file.

---

## 🚀 Lab Walkthrough

### Module 1: John the Ripper (Johnny GUI)
The first approach involved using the Johnny GUI (a graphical frontend for John the Ripper) on a Windows environment. 

**Process:**
1. Opened the password-protected PDF using Johnny.
2. Extracted the `$pdf$` hash format.
3. Executed a dictionary attack using a standard wordlist.
4. **Result:** The password was successfully cracked.

*Screenshot of the successful Johnny GUI crack:*
![Johnny GUI Crack Success](images/01_johnny_gui_success.png)

---

### Module 2: Networkwalks Browser-Based Tools
To validate the process and remove the need for local installations, the exact same challenge was executed using Networkwalks' web-based utilities.

#### Step 2.1: Extracting the PDF Hash
Using the Networkwalks Hash Calculator, the hash was extracted directly in the browser (no files were uploaded to a server).

*Screenshot of the Hash Calculator Interface:*
![Networkwalks Hash Calculator](images/02_networkwalks_hash_calc.png)

#### Step 2.2: Executing the Dictionary Attack
The extracted hash was pasted into the Networkwalks Password Cracker. The tool runs the dictionary attack in real-time, logging the attempted words.

*Screenshot of the Dictionary Attack in progress and successful crack:*
![Networkwalks Password Cracker](images/03_networkwalks_password_cracker.png)

---

## 💡 Key Takeaways & Insights

1. **Encryption is reversible; Hashing is one-way.** 
   - Encryption hides data using a key, which can be recovered. 
   - Hashing is a one-way mathematical function. However, because users create weak passwords, an attacker can just "guess" the input and see if the hash matches.

2. **The Illusion of Hash Security:** 
   - A strong hashing algorithm (like SHA-256) protects the *storage* of the password, but it cannot protect against a *weak human choice*. Passwords like `"password1"` or simple words from the dictionary will fold in seconds.

3. **The Power of Dictionary Attacks:**
   - Brute-forcing every possible character combination is slow. Using a targeted dictionary of common passwords is incredibly fast and highly effective.

4. **Defense:** 
   - Use strong, unique passphrases. Implement Multi-Factor Authentication (MFA). Never rely solely on hashing as your security net for user credentials.

---

## 🎓 Acknowledgements
This lab was completed as part of the **Cybersecurity & Ethical Hacking** training program at [NETWORKWALKS Training Academy](https://networkwalks.com/). Their lab-driven approach makes complex concepts like hash extraction and dictionary attacks highly practical and easy to understand.

---
**Disclaimer:** This repository is for educational purposes only. The techniques demonstrated here should only be used on systems you own or have explicit permission to test.
