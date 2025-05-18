# MITRE ATT&CK Navigator Mapping

## Plik: `lab-detection-mapping.json`

Ten plik został przygotowany do zaimportowania w [MITRE ATT&CK Navigator](https://mitre-attack.github.io/attack-navigator/). Obejmuje on reguły przetestowane w ramach projektu `defender-lab-setup`.

### Legenda kolorów:

- 🟩 `#66ff66` – Reguła przetestowana i wykrywana (alert obecny, także w środowisku produkcyjnym)

### Objęte reguły:

| Technika ATT&CK | ID            | Komentarz |
|------------------|---------------|-----------|
| Windows Management Instrumentation Subscription | T1546.003 | `ASR-WMI-Test.md` |
| Create Account + Account Manipulation + Valid Accounts | T1136, T1098, T1078 | `1_local_account_created_deleted.md` |
| Local Group Enumeration + Account Manipulation + Valid Accounts | T1069.001, T1098, T1078 | `2_UserAccountAddedToLocalGroup_RemovedFromLocalGroup.md` |

---

### Jak zaimportować:

1. Wejdź na [MITRE Navigator](https://mitre-attack.github.io/attack-navigator/)
2. Kliknij: **Open Existing Layer**
3. Wybierz plik `lab-detection-mapping.json`
4. Gotowe!

---

###  Uwagi

- Mapowanie dotyczy wyłącznie reguł, które zostały **przetestowane**.
- Przypisanie technik zostało wykonane szeroko (multi-tagging), aby odzwierciedlić rzeczywiste pokrycie.

