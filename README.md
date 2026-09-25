**PASSWORD RECOVERY & HASH ANALYSIS: JOHN THE RIPPER(JTR) APP AND NETWORKWALKS TOOLS**




Project Overview
This project demonstrates the process of auditing, extracting, 
and cracking password-protected PDF documents using offline and web-based hash cracking techniques.
By leveraging the John the Ripper (JTR) Application and NETWORKWALKS Tools, 
this lab demonstrates how cryptographic hashes are generated from encrypted documents, 
extracted, and subjected to dictionary and brute-force attacks to recover credentials.


**OBJECTIVES**
* Understand Hash Extraction: Learn how security handlers encrypt PDF files and how cryptographic signatures are represented   in hash formats.

* Offline Hash Cracking: Execute dictionary and brute-force attacks using the John the Ripper application against extracted    PDF hashes.

* Online Hash Cracking: Utilize browser-based utilities (NETWORKWALKS Tools) for lightweight online password recovery
  workflows.

* Credential Verification: Validate recovered passwords by successfully decrypting and accessing the protected original
  documents.

* Security Assessment: Evaluate password strength and understand why short or predictable passwords fail against hash-
  cracking utilities.


**SECURITY AND ETHICAL USE**
DISCLAIMER: The techniques, software, and tools documented in this repository are for educational purposes, authorized security testing, and personal credential recovery only. Executing password attacks against systems or files without explicit permission from the owner is illegal and violates cybersecurity ethics.




**INTRODUCTION TO PASSWORD CRACKING**
Password cracking is the process of recovering plain-text passwords from stored cryptographic hashes or encrypted containers. Modern applications do not store actual passwords directly; instead, they store a mathematical hash or use encryption keys derived from the password.

When attempting to access an encrypted document (like a protected PDF), an auditor cannot read the file contents directly. Instead, the process involves:

* Extracting the document's encryption parameters and hash structure.

* Passing the extracted hash to a cracking engine (such as the John the Ripper application).

* Generating candidate passwords, hashing them, and comparing them against the target hash until a match is discovered.




**TECHNICAL EXECUTION & METHODOLOGY**
Method 1: Offline Attack via John the Ripper (JTR) App
Step 1: Hash Extraction via Online PDF Hash Converter
* Uploaded the target password-protected PDF file to an online hash extraction utility to convert the file header into a crackable hash string.

* Exported and saved the resulting hash output into a plain-text file.

![Hash Coverter](Screenshot%2026-09-23-090219)

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

[PLACEHOLDER: Insert screenshot of the NETWORKWALKS Hash Calculator output displaying the $pdf$ hash]

Step 2: Cracking via NETWORKWALKS Password Cracker
Opened a web browser and navigated to the NETWORKWALKS Password Cracker interface.

Pasted the full $pdf$ hash string into the designated hash input field.

Clicked Start Attack. The tool initiated an automated sequence trying candidate passwords until a match was identified.

Received the interface message: "Password cracked successfully" along with the plain-text credential.

[PLACEHOLDER: Insert screenshot of the NETWORKWALKS Password Cracker showing the "Password cracked successfully" result]

Step 3: Document Decryption Verification
Copied the recovered plain-text password from the NETWORKWALKS interface.

Applied the credential to the original PDF file, confirming full document decryption and access.

[PLACEHOLDER: Insert screenshot showing the decrypted PDF content]

What I Learned
Hash Structure Standardization: Identified how PDF encryption signatures are structured with explicit identifiers (such as $pdf$) that inform cracking engines of the underlying encryption scheme (e.g., AES or RC4).

Offline vs. Online Cracking Workflows: Offline cracking using dedicated applications like JTR allows for local processing and custom wordlists, while online utilities like NETWORKWALKS provide quick, accessible web-based interfaces for hash matching.

Impact of Password Entropy: Observed firsthand how simple or dictionary-based passwords can be cracked quickly, reinforcing the necessity of complex passphrases and strong organizational password policies.

Issues Faced During the Project
Hash Formatting Errors: Initially encountered issues where the copied hash string omitted structural delimiters, preventing the JTR application from parsing the hash properly. Ensuring the complete $pdf$...string was preserved resolved the error.

Wordlist Coverage Limits: Default short wordlists failed to resolve the hash during early test iterations. Loading a broader dictionary into the application resolved the match.

Browser Session Timeouts: During online cracking with NETWORKWALKS Tools, larger wordlist lookups occasionally caused browser latency. Testing with targeted hash sets ensured smooth operation.

Tools Used
John the Ripper (JTR) App: Offline GUI application for password recovery and hash cracking.

Online PDF Hash Extractor: Web utility used to parse protected PDF files and export crackable hash strings.

NETWORKWALKS Hash Calculator: Online tool for extracting signature hashes starting with $pdf$.

NETWORKWALKS Password Cracker: Web-based cracking interface for online hash attacks.

Wordlist Dictionary: Custom/standard wordlists used for password candidate generation.




**Author**
Esther Mesirionye
Cybersecurity Intern at Networkwalks
