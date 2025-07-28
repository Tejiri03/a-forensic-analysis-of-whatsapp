# 📱 Forensic Analysis of WhatsApp on Android

This is a forensic analysis report of the WhatsApp Messenger application on an Android device, following the NIST 800-101 Rev.1 guidelines. The report was completed as part of the MSc Cybersecurity module "Forensics and eDiscovery" at the National College of Ireland.

---

## 📝 Executive Summary

This analysis examines WhatsApp's internal file structure, cryptographic security, and key forensic artifacts including chat history, contact data, media metadata, and encryption keys. Tools such as Android Studio, APKTool, JADX, ADB, and SQLite Browser were used in a virtualized test environment on macOS.

---

## 🧪 Methodology

- **Framework Used**: NIST 800-101
- **Phases**: Identification, Acquisition, Analysis, Reporting
- **Environment**: macOS (M1), Android Emulator (AVD)
- **APK Version**: 2.25.5.17

---

## 📂 Key Databases Analyzed

| Database       | Description |
|----------------|-------------|
| `msgstore.db`  | Stores chat messages, timestamps, and metadata |
| `wa.db`        | Contact info, group membership |
| `axolotl.db`   | Signal protocol keys |
| `media.db`     | Media metadata |
| `location.db`  | Shared location logs |

---

## 🔧 Tools Used

- Android Studio (Emulator)
- APKTool (Static APK analysis)
- JADX (DEX to Java decompilation)
- ADB (Data extraction)
- SQLite Browser (DB inspection)

---

## 🔍 Findings Summary

- WhatsApp uses multiple `.db` files to store user data.
- End-to-end encryption is implemented using the Signal Protocol.
- Key artifacts can be extracted with root access and forensic tools.
- SQLite files include valuable metadata and user interactions.

---

## 📌 Limitations

- Rooting and emulator performance issues
- Some encrypted files could not be decrypted
- Access restrictions due to Android security policies

---
