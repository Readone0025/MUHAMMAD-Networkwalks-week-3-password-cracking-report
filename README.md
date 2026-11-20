<div align="center">

# 🔐 Password Cracking Report

**John the Ripper (JTR) & Networkwalks Tools**

*Cybersecurity Internship · Networkwalks · Week 03*

</div>

<p align="center">
  <img src="https://img.shields.io/badge/Project-W3--PM1%20%26%20W3--PM2-C00000?style=flat-square&labelColor=404040" />
  <img src="https://img.shields.io/badge/Focus-Password%20Cracking-0070C0?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Tools-Johnny%20%7C%20NW%20Hash%20Calculator%20%7C%20Password%20Cracker-E87500?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Status-Completed-28a745?style=flat-square&labelColor=404040" />
</p>

---

| | |
|---|---|
| **Pentester Name (Cybersecurity Intern)** | Muhammad Ahmad Abdullahi |
| **Program / Batch** | B084 · Networkwalks |
| **Report Date** | 20 November 2026 |
| **Modules Completed** | W3-PM1 (Password Cracking with JTR / Johnny) · W3-PM2 (Password Cracking with Networkwalks Tools) |
| **Target Files** | My Locked PDF1.pdf · My Locked PDF2.pdf · My Locked PDF3.pdf |
| **Authorization** | Authorized lab exercise under Networkwalks Internship Program |

---

## 📑 Table of Contents

1. [Liability Disclaimer](#1-liability-disclaimer)
2. [Introduction](#2-introduction)
3. [Tools Used](#3-tools-used)
4. [Activities Performed](#4-activities-performed)
5. [Results & Captured Flags](#5-results--captured-flags)
6. [Risk Analysis / Impact](#6-risk-analysis--impact)
7. [Recommendations](#7-recommendations)
8. [Conclusion](#8-conclusion)
9. [Evidences Collected](#9-evidences-collected)

---

## 1. Liability Disclaimer

> ⚠️ All activities documented in this report were performed strictly within the scope of authorized Networkwalks lab exercises. The password-protected PDF files used are training materials provided by the program. This work is for **educational purposes only**. Unauthorized password cracking or attempts against systems you do not own or have explicit permission to test is illegal. The author, instructors, and Networkwalks accept no responsibility for misuse of the knowledge demonstrated here.

---

## 2. Introduction

This report documents the successful completion of **Week 3 Project Modules** of the Networkwalks Cybersecurity Internship (Batch B084).

The objective was to recover the password of encrypted PDF files using two different approaches:

- **W3-PM1**: Offline password cracking with **John the Ripper** (via the Johnny GUI)
- **W3-PM2**: Online password cracking using **Networkwalks Hash Calculator** and **Password Cracker**

Additional practice was also performed by extracting hashes from two further locked PDF files (PDF2 and PDF3) using OnlineHashCrack.

The exercises demonstrate how weak passwords can be recovered quickly and highlight the importance of strong password practices when protecting sensitive documents.

---

## 3. Tools Used

| Tool | Purpose |
|------|---------|
| **Johnny** (GUI for John the Ripper) | Offline cracking of PDF password hashes |
| **Networkwalks Hash Calculator** | Extract `\( pdf \)` hash from password-protected PDF |
| **Networkwalks Password Cracker** | Dictionary-based attack against extracted PDF hash |
| **OnlineHashCrack** | Alternative PDF hash extraction (used for PDF2 & PDF3) |
| **PDF Reader** | Opening the decrypted files to capture flags |

---

## 4. Activities Performed

### 4.1 Module 1 – Password Cracking with JTR (Johnny)

**Objective:** Crack the password of the protected PDF using John the Ripper (Johnny GUI).

#### Steps Performed

1. Extracted the PDF hash and saved it to a text file.
2. Opened Johnny and loaded the hash file.
3. Configured the path to `john.exe`.
4. Started a new attack.
5. Successfully recovered the password.

**Result**

- **Cracked Password**: `password1`
- Status: `100% (1/1) cracked`

![Johnny – Hash Loaded](images/01-johnny-hash-loaded.png)

![Johnny – Password Cracked](images/02-johnny-password-cracked.png)

**Why it matters:** Offline tools such as John the Ripper allow security professionals to test password strength without relying on external services. Weak passwords can be recovered in a short time, demonstrating the risk of using simple or common passwords.

---

### 4.2 Module 2 – Password Cracking with Networkwalks Tools

**Objective:** Crack the same PDF using the free browser-based tools provided by Networkwalks.

#### Steps Performed

1. Uploaded `My Locked PDF1.pdf` to the Networkwalks Hash Calculator.
2. Copied the full `\( pdf \)` hash.
3. Pasted the hash into the Networkwalks Password Cracker.
4. Started the dictionary attack.
5. Successfully recovered the password.

**Result**

- **Cracked Password**: `password1`

![Networkwalks Hash Calculator](images/03-hash-calculator-pdf1.png)

![Networkwalks Password Cracker – Success](images/04-password-cracker-success.png)

**Why it matters:** Browser-based tools make password cracking accessible for training purposes. They clearly show the two-stage process of hash extraction followed by dictionary attack.

---

### 4.3 Additional Practice – PDF2 & PDF3

Hashes were also extracted from two additional locked PDF files using **OnlineHashCrack** for further practice.

#### My Locked PDF2

![OnlineHashCrack – PDF2](images/07-onlinehashcrack-pdf2.png)

#### My Locked PDF3

![OnlineHashCrack – PDF3](images/08-onlinehashcrack-pdf3.png)

---

## 5. Results & Captured Flags

After successfully cracking the passwords and opening the protected PDFs, the following flags were captured:

| Flag | Description |
|------|-------------|
| `nw{password_cracking_flag_success_1}` | First successfully opened PDF |
| `nw{cybersecurity_flag_captured_2026}` | Additional flag from opened PDF |
| `nw{password_cracking_success_WK3-PM2}` | Flag obtained via Networkwalks Tools module |

![PDF Opened – Flag 1](images/05-pdf1-opened-flag.png)

![PDF Opened – PM2 Flag](images/06-pdf-opened-flag-pm2.png)

---

## 6. Risk Analysis / Impact

| # | Finding | Observation | Potential Impact | Risk Level |
|---|---------|-------------|------------------|------------|
| 1 | Weak password used | Password `password1` was recovered almost immediately | Sensitive documents protected by weak passwords can be opened by anyone with basic tools | 🔴 High |
| 2 | Hash extraction is straightforward | Multiple free tools successfully extracted the `\( pdf \)` hash | Once the hash is obtained, offline and online cracking becomes possible | 🟠 Medium |
| 3 | Dictionary attacks remain effective | Common passwords are still present in wordlists | Users who reuse simple passwords are highly vulnerable | 🔴 High |
| 4 | Multiple tools available | Both offline (Johnny) and online tools succeeded | Attackers have many easy options to recover weak PDF passwords | 🟠 Medium |

**Risk level key:** 🔴 High · 🟠 Medium · 🟢 Low

> ℹ️ The password used in this lab was intentionally weak for training purposes. In real-world scenarios, the same techniques can recover poorly chosen passwords protecting confidential documents.

---

## 7. Recommendations

- **Use strong passwords**: Prefer long, unique passphrases that combine uppercase, lowercase, numbers, and symbols.
- **Avoid common passwords**: Never use passwords such as `password1`, `123456`, or simple dictionary words.
- **Enable multi-factor protection** where possible (some PDF tools support additional security layers).
- **Educate users**: Staff should understand that document encryption is only as strong as the password chosen.
- **Regularly review password policies**: Encourage the use of password managers to generate and store strong credentials.
- **Limit sharing of encrypted files**: Only share password-protected documents with authorized recipients through secure channels.

---

## 8. Conclusion

In Week 3 of the Cybersecurity Internship I successfully completed both essential password cracking modules.

Using **Johnny (John the Ripper)**, I performed offline cracking and recovered the password `password1`. Using the **Networkwalks Hash Calculator** and **Password Cracker**, I repeated the process with browser-based tools and obtained the same result. I also practiced hash extraction on two additional locked PDF files.

The exercises clearly demonstrated that weak passwords provide little real protection. Once a hash is extracted, modern tools can recover simple passwords very quickly. This reinforces the critical importance of strong password practices when securing sensitive documents.

All activities were performed strictly within the authorized Networkwalks lab environment for educational purposes.

---

## 9. Evidences Collected

| # | Evidence | File |
|---|----------|------|
| 1 | Johnny – Hash loaded | `images/01-johnny-hash-loaded.png` |
| 2 | Johnny – Password cracked | `images/02-johnny-password-cracked.png` |
| 3 | Networkwalks Hash Calculator | `images/03-hash-calculator-pdf1.png` |
| 4 | Networkwalks Password Cracker success | `images/04-password-cracker-success.png` |
| 5 | PDF opened – Flag 1 | `images/05-pdf1-opened-flag.png` |
| 6 | PDF opened – PM2 Flag | `images/06-pdf-opened-flag-pm2.png` |
| 7 | OnlineHashCrack – PDF2 | `images/07-onlinehashcrack-pdf2.png` |
| 8 | OnlineHashCrack – PDF3 | `images/08-onlinehashcrack-pdf3.png` |

---

<div align="center">

*- End -*

</div>

## 👤 Author

**Muhammad Ahmad Abdullahi**  
Cybersecurity Intern · Batch B084  
GitHub: `https://github.com/Readone0025` · LinkedIn: `https://www.linkedin.com/in/muhammad-ahmad-2a6057447`

## 📌 Project Information

**Program:** Cybersecurity program at Networkwalks | **Week:** 03 | **Repository:** GitHub