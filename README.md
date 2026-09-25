Password Recovery & Hash Analysis: John the Ripper (JTR) App & NETWORKWALKS Tools





Project Overview
This project demonstrates the process of auditing, extracting, and cracking password-protected PDF documents using offline and web-based hash cracking techniques. By leveraging the John the Ripper (JTR) Application and NETWORKWALKS Tools, this lab demonstrates how cryptographic hashes are generated from encrypted documents, extracted, and subjected to dictionary and brute-force attacks to recover credentials.




Objectives


Understand Hash Extraction: Learn how security handlers encrypt PDF files and how cryptographic signatures are represented in hash formats.

Offline Hash Cracking: Execute dictionary and brute-force attacks using the John the Ripper application against extracted PDF hashes.

Online Hash Cracking: Utilize browser-based utilities (NETWORKWALKS Tools) for lightweight online password recovery workflows.

Credential Verification: Validate recovered passwords by successfully decrypting and accessing the protected original documents.

Security Assessment: Evaluate password strength and understand why short or predictable passwords fail against hash-cracking utilities.




Security and Ethical Use
DISCLAIMER: The techniques, software, and tools documented in this repository are for educational purposes, authorized security testing, and personal credential recovery only. Executing password attacks against systems or files without explicit permission from the owner is illegal and violates cybersecurity ethics.




Introduction to Password Cracking
Password cracking is the process of recovering plain-text passwords from stored cryptographic hashes or encrypted containers. Modern applications do not store actual passwords directly; instead, they store a mathematical hash or use encryption keys derived from the password.

When attempting to access an encrypted document (like a protected PDF), an auditor cannot read the file contents directly. Instead, the process involves:

*Extracting the document's encryption parameters and hash structure.

*Passing the extracted hash to a cracking engine (such as the John the Ripper application).

*Generating candidate passwords, hashing them, and comparing them against the target hash until a match is discovered.




Technical Execution & Methodology


Method 1: Offline Attack via John the Ripper (JTR) App

Step 1: Hash Extraction via Online PDF Hash Converter
*Uploaded the target password-protected PDF file to an online hash extraction utility to convert the file header into a crackable hash string.

*Exported and saved the resulting hash output into a plain-text file.
[PLACEHOLDER: Insert screenshot showing the online hash extractor generating the PDF hash]

Step 2: Executing John the Ripper App
Launched the John the Ripper (JTR) App.
Imported the saved hash file into the application interface.
Selected the target wordlist dictionary and initiated the cracking attack session.
The JTR app processed the candidate passwords until a match was identified.
[PLACEHOLDER: Insert screenshot of the JTR application running and displaying the cracked password]

Step 3: Verifying Document Access
Copied the recovered plain-text password from the JTR app.
Opened the original protected PDF file, supplied the cracked password, and successfully unlocked the document.
[PLACEHOLDER: Insert screenshot of the unlocked PDF document opened with the cracked password]

Method 2: Web-Based Attack via NETWORKWALKS Tools
Step 1: Generating the Hash via Hash Calculator
Navigated to the NETWORKWALKS Hash Calculator tool.
Uploaded the target encrypted PDF file to extract its cryptographic hash signature.
Received the extracted hash string starting with the $pdf$ format prefix.
Copied the complete hash string to the clipboard.
[PLACEHOLDER: Insert screenshot of the NETWORKWALKS Hash Calcula…# Password-Cracking-with-John-The-Ripper-and-Networkwalks-Tools-Tools.
A Project on how to crack a file and get its password.
