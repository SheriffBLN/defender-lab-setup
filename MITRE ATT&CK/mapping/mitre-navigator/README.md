# MITRE ATT&CK Navigator Mapping

## Plik: `lab-detection-mapping.json`

Ten plik został przygotowany do zaimportowania w [MITRE ATT&CK Navigator](https://mitre-attack.github.io/attack-navigator/). Obejmuje on reguły przetestowane w ramach projektu `defender-lab-setup`.

---

## 🎨 Legenda kolorów:

- 🟩 `#66ff66` – Reguła przetestowana i wykrywana (alert obecny, także w środowisku produkcyjnym)
- 🟨 `#ffff66` – Reguła ASR uruchomiona w trybie audit, ale **jeszcze nie została przetestowana** (oznaczenie wstępne do przyszłych testów)

---

## ✅ Objęte reguły (przetestowane):

| Technika ATT&CK | ID | Taktyka ATT&CK | Komentarz |
|------------------|----|----------------|-----------|
| Windows Management Instrumentation Subscription | T1546.003 | Persistence | ASR-WMI-Test.md |
| Create Account | T1136 | Persistence | 1_local_account_created_deleted.md |
| Account Manipulation | T1098 | Privilege Escalation, Defense Evasion | 1_local_account_created_deleted.md, 2_UserAccountAddedToLocalGroup_RemovedFromLocalGroup.md, 3_LocalUserAccountModified.md |
| Valid Accounts | T1078 | Defense Evasion, Persistence | 1_local_account_created_deleted.md, 2_UserAccountAddedToLocalGroup_RemovedFromLocalGroup.md |
| User Account Management | T1087.001 | Discovery | 3_LocalUserAccountModified.md |
| Account Access Removal | T1531 | Defense Evasion, Impact | 1_local_account_created_deleted.md |

---

## 🟨 Reguły ASR w trybie audit:

| Technika ATT&CK | ID | Taktyka ATT&CK | Komentarz |
|------------------|----|----------------|-----------|
| Exploitation for Privilege Escalation | T1068 | Privilege Escalation | ASR: Block abuse of exploited vulnerable signed drivers |
| LSASS Memory | T1003.001 | Credential Access | ASR: Block credential stealing from LSASS |
| Malicious File | T1204.002 | Execution | ASR: Block executable content from email and webmail |
| Office Child Processes | T1059.005 | Execution | ASR: Block Office apps from creating child processes |
| Process Injection | T1055.001 | Defense Evasion | ASR: Block Office apps from injecting code |
| Office Comm Apps | T1059.001 | Execution | ASR: Block Office communication app from creating child processes |
| JavaScript/VBScript | T1204.002 | Execution | ASR: Block JavaScript/VBScript from launching content |
| Obfuscated Scripts | T1027 | Defense Evasion | ASR: Block execution of potentially obfuscated scripts |
| Win32 API from Macros | T1059.005 | Execution | ASR: Block Win32 API calls from Office macros |
| Ransomware Protection | T1486 | Impact | ASR: Use advanced protection against ransomware |
| SMB Credential Stealing | T1555.003 | Credential Access | ASR: Block credential stealing via SMB |

---

##  Jak zaimportować:

1. Wejdź na [MITRE Navigator](https://mitre-attack.github.io/attack-navigator/)
2. Kliknij: **Open Existing Layer**
3. Wybierz plik `lab-detection-mapping.json`
4. Gotowe!

---

##  Uwagi

- Mapowanie dotyczy tylko reguł przetestowanych (🟩) oraz reguł z trybem audit (🟨).
- Przypisanie technik i taktyk zostało przeprowadzone z uwzględnieniem kontekstu operacyjnego i możliwych celów atakujących.
