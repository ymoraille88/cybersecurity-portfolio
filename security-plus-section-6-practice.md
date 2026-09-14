# Security+ Learning Portfolio: Signs of Attacks

Study record prepared September 14, 2026.

Course: [CompTIA Security+ SY0-701 — Andrew Ramdayal / TIA Training](https://www.udemy.com/course/comptia_security_plus/). Section 6: Signs of Attacks.

## Practice results

Completed two guided rounds of original practice questions in this conversation. These are learning exercises, not official CompTIA questions or Udemy quiz results. Feedback was provided after every answer, and some concepts were repeated.

| Activity | Result |
| --- | --- |
| Round 1: Malware identification | 9/10 (90%) |
| Round 2: Applied scenarios | 9/10 (90%) |
| Combined | 18/20 (90%) |

Practiced identifying worms, viruses, Trojans, ransomware, spyware, rootkits, logic bombs, and keyloggers. Additional scenarios covered cryptojacking, containment, behavioral detection, and double extortion. These results document guided practice rather than independently verified exam readiness.

## Round 1 question record

Questions below retain the scenarios and answer choices from the conversation, with minor wording compression.

| # | Question | Choices | My answer | Correct answer |
| --- | --- | --- | --- | --- |
| 1 | Malware automatically spreads between computers by exploiting a network service vulnerability, without users opening files or running programs. What is it? | A. Trojan; B. Worm; C. Logic bomb; D. File-infecting virus | B | B — Worm |
| 2 | A downloaded PDF converter secretly gives an attacker remote access when installed. What is it? | A. Worm; B. Trojan; C. Logic bomb; D. Spyware | B | B — Trojan |
| 3 | Malicious code deletes company files if a particular employee's account is disabled. What is it? | A. Ransomware; B. Rootkit; C. Logic bomb; D. Worm | B | C — Logic bomb |
| 4 | Malware sends users' keystrokes to an attacker, capturing typed passwords. What most specifically describes it? | A. Keylogger; B. Ransomware; C. Worm; D. Rootkit | A | A — Keylogger |
| 5 | Employees cannot open their files and receive a demand for payment in exchange for a decryption key. What is it? | A. Spyware; B. Logic bomb; C. Ransomware; D. Trojan | C | C — Ransomware |
| 6 | Malware conceals malicious files and processes while maintaining administrator-level access. What is it? | A. Rootkit; B. Worm; C. Ransomware; D. Keylogger | A | A — Rootkit |
| 7 | A malicious program attaches to an executable and infects other executable files when the user runs it. What is it? | A. Worm; B. Virus; C. Trojan; D. Logic bomb | B | B — Virus |
| 8 | Software secretly collects browsing history, takes screenshots, and transmits information to a third party. What is it? | A. Ransomware; B. Worm; C. Spyware; D. Logic bomb | C | C — Spyware |
| 9 | A slow workstation has high CPU usage and an unauthorized cryptocurrency mining process. What is this activity? | A. Cryptojacking; B. Keylogging; C. Ransomware; D. Logic bomb | A | A — Cryptojacking |
| 10 | Malicious code remains inactive until a specific date, then deletes backup files. What is it? | A. Rootkit; B. Trojan; C. Logic bomb; D. Worm | C | C — Logic bomb |

## Round 2 question record

| # | Question | Choices | My answer | Correct answer |
| --- | --- | --- | --- | --- |
| 1 | An employee enables macros in a spreadsheet; malicious code runs and infects other spreadsheets. What is it? | A. Worm; B. Macro virus; C. Rootkit; D. Logic bomb | B | B — Macro virus |
| 2 | Malware modifies operating system components to hide files and processes from security tools, persisting after suspicious applications are removed. What is it? | A. Spyware; B. Ransomware; C. Rootkit; D. Macro virus | C | C — Rootkit |
| 3 | A free browser extension secretly records browsing activity and sends screenshots externally. What best describes its primary function? | A. Trojan; B. Spyware; C. Worm; D. Ransomware | B | B — Spyware |
| 4 | Malware spreads between servers without user interaction. What best limits spread during cleanup? | A. Change employee passwords; B. Isolate infected servers from the network; C. Disable spreadsheet macros; D. Increase backup frequency | B | B — Isolate infected servers |
| 5 | A script checks payroll daily and deletes critical files if its creator's name disappears. What is the key logic bomb clue? | A. Runs daily; B. Accesses sensitive information; C. Destruction depends on a specific condition; D. Creator is an employee | C | C — Conditional trigger |
| 6 | A fake software update encrypts files and demands payment. What describes delivery and function? | A. Trojan delivering ransomware; B. Worm delivering spyware; C. Rootkit delivering a macro virus; D. Logic bomb delivering a keylogger | A | A — Trojan delivering ransomware |
| 7 | A tool flags a new program for rapidly modifying files and disabling recovery, without a known malware signature. Which detection method is used? | A. Signature-based detection; B. Behavior-based detection; C. File hash matching; D. Manual code review | B | B — Behavior-based detection |
| 8 | An employee autofills a password instead of typing it. Which malware capability is most directly bypassed? | A. Recording individual keystrokes; B. Capturing screenshots; C. Stealing session cookies; D. Reading credentials from browser memory | D | A — Recording individual keystrokes |
| 9 | After files are restored from ransomware, the attacker threatens to publish documents stolen before encryption. What does this demonstrate? | A. False positive; B. Double extortion; C. Logic bomb; D. Resource exhaustion | B | B — Double extortion |
| 10 | An attachment executes malware that then independently exploits network services to copy itself between computers. Which characteristic identifies the worm component? | A. Arrived through email; B. Conceals itself in a legitimate file; C. Spreads without further user action; D. Executes only on a specific date | C | C — Autonomous spread |

## Corrections and learning notes

- **Logic bomb versus rootkit:** A logic bomb activates on a condition, such as an account being disabled or a date arriving. A rootkit hides malicious activity and supports continued privileged access. After missing Round 1 Question 3, I correctly identified logic bombs in Round 1 Question 10 and Round 2 Question 5.
- **Autofill versus keylogging:** Autofill avoids manually typing a password, bypassing basic keystroke-only capture. It does not protect against all credential theft; malware may read browser memory or capture form values through other mechanisms. This concept needs another practice check.
- **Delivery versus function:** A Trojan describes deceptive software presentation. The delivered payload may perform spyware or ransomware functions.
- **Containment:** Isolating infected systems limits network spread while cleanup proceeds.
- **Double extortion:** Backups help recover encrypted files but do not reverse data theft or the threat of publication.

## Udemy practice tests

The learner reports taking the following five quizzes. Their titles, questions, scores, and completion dates were not accessible from the supplied links and remain pending. No Udemy results are included in the 18/20 conversation practice total.

| Quiz reference | Link | Score / title |
| --- | --- | --- |
| 6180122 | [Open Udemy quiz](https://www.udemy.com/course/comptia_security_plus/learn/quiz/6180122#overview) | Pending learner results |
| 6180118 | [Open Udemy quiz](https://www.udemy.com/course/comptia_security_plus/learn/quiz/6180118#overview) | Pending learner results |
| 6180116 | [Open Udemy quiz](https://www.udemy.com/course/comptia_security_plus/learn/quiz/6180116#overview) | Pending learner results |
| 6180064 | [Open Udemy quiz](https://www.udemy.com/course/comptia_security_plus/learn/quiz/6180064#overview) | Pending learner results |
| 6180068 | [Open Udemy quiz](https://www.udemy.com/course/comptia_security_plus/learn/quiz/6180068#overview) | Pending learner results |

Next update: add each Udemy quiz's title, earned score, total questions, completion date if available, and concepts missed.
