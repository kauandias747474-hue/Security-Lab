# 🔒 Lab: Identifying Obsolete Cryptography

### 🇧🇷 Cenário: Cifras Legadas
Identificação de tráfego ou armazenamento de dados que utiliza algoritmos quebrados como DES ou MD5. O objetivo é demonstrar a facilidade de recuperação de dados quando a criptografia não acompanha a evolução computacional.

### 🇺🇸 Scenario: Legacy Ciphers
Identifying traffic or data storage using broken algorithms like DES or MD5. The goal is to demonstrate how easily data can be recovered when cryptography fails to evolve alongside computational power.

## 🛡️ Mitigação
* Substituição por **AES-256-GCM** ou **ChaCha20**.
* Uso de TLS 1.3 para comunicações em trânsito.
