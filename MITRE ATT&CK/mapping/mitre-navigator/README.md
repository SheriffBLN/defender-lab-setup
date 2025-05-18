# MITRE ATT&CK Navigator Mapping

## Plik: `lab-detection-mapping.json`

Ten plik został przygotowany do zaimportowania w [MITRE ATT&CK Navigator](https://mitre-attack.github.io/attack-navigator/). Obejmuje on reguły przetestowane w ramach projektu `defender-lab-setup`.

---

## 🎨 Legenda kolorów:

- 🟩 `#66ff66` – Reguła przetestowana i wykrywana (alert obecny, także w środowisku produkcyjnym)
- 🟨 `#ffff66` – Reguła ASR uruchomiona w trybie audit, ale **jeszcze nie została przetestowana** (oznaczenie wstępne do przyszłych testów)

---

##  Objęte reguły (przetestowane):

| Technika ATT&CK | ID            | Komentarz |
|------------------|---------------|-----------|
| Windows Management Instrumentation Subscription | T1546.003 | `ASR-WMI-Test.md` |
| Create Account + Account Manipulation + Valid Accounts | T1136, T1098, T1078 | `1_local_account_created_deleted.md` |
| Local Group Enumeration + Account Manipulation + Valid Accounts | T1069.001, T1098, T1078 | `2_UserAccountAddedToLocalGroup_RemovedFromLocalGroup.md` |
| User Account Enumeration + Account Manipulation | T1087.001, T1098 | `3_LocalUserAccountModified.md` |

---

##  Reguły ASR w trybie audit:

| Technika ATT&CK | ID            | Komentarz |
|------------------|---------------|-----------|
| Exploitation for Privilege Escalation | T1068 | ASR: Block abuse of exploited vulnerable signed drivers |
| LSASS Memory | T1003.001 | ASR: Block credential stealing from LSASS |
| Malicious File | T1204.002 | ASR: Block executable content from email and webmail |
| Office Child Processes | T1059.005 | ASR: Block Office apps from creating child processes |
| Process Injection | T1055.001 | ASR: Block Office apps from injecting code |
| Office Comm Apps | T1059.001 | ASR: Block Office communication app from creating child processes |
| JavaScript/VBScript | T1204.002 | ASR: Block JavaScript/VBScript from launching content |
| Obfuscated Scripts | T1027 | ASR: Block execution of potentially obfuscated scripts |
| Win32 API from Macros | T1059.005 | ASR: Block Win32 API calls from Office macros |
| Ransomware Protection | T1486 | ASR: Use advanced protection against ransomware |
| SMB Credential Stealing | T1555.003 | ASR: Block credential stealing via SMB |

---

## Jak zaimportować:

1. Wejdź na [MITRE Navigator](https://mitre-attack.github.io/attack-navigator/)
2. Kliknij: **Open Existing Layer**
3. Wybierz plik `lab-detection-mapping.json`
4. Gotowe!

---

##  Uwagi

- Mapowanie dotyczy tylko reguł przetestowanych (🟩) oraz reguł z trybem audit (🟨).
- Przypisanie technik zostało wykonane szeroko (multi-tagging), aby odzwierciedlić rzeczywiste pokrycie.
