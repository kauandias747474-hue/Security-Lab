# 💾 Lab: Insecure Local Storage & Forensic Analysis

### 🇧🇷 Diagnóstico: Armazenamento Local Inseguro
Muitas vezes, dados sensíveis como tokens de sessão ou informações pessoais (PII) são guardados sem criptografia em ficheiros locais. Este laboratório foca na extração forense de dados a partir da sandbox do utilizador.

### 🇺🇸 Diagnostic: Insecure Local Storage
Often, sensitive data such as session tokens or PII are stored without encryption in local files. This lab focuses on forensic data extraction from the user's sandbox.

---

## 🔬 O Ataque | The Attack
1. Utiliza-se o **ADB (Android Debug Bridge)** para aceder ao sistema de ficheiros.
2. Exploração da pasta `/data/data/[package.name]/shared_prefs`.
3. Leitura de ficheiros XML e bases de dados SQLite que contêm credenciais em texto limpo.

## 🛠️ Estrutura do Lab
* `extract-data.py`: Script automatizado via ADB para recolha de ficheiros sensíveis.
* `db-viewer.sql`: Queries para demonstrar a presença de PII em bases de dados locais.

## 🛡️ Mitigação
* Uso de APIs de armazenamento seguro como **EncryptedSharedPreferences** ou **Android Keystore System**.
* Criptografia de base de dados SQLite (SQLCipher).

---
