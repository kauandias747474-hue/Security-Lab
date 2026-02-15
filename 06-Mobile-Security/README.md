# 📱 Mobile App Security | Segurança de Apps Móveis

### 🇧🇷 Análise de Segurança em Ecossistemas Mobile (Android/iOS)
Diferente das aplicações Web, os apps móveis residem no dispositivo do usuário, o que os torna alvos de engenharia reversa e manipulação em tempo real. Este módulo foca na análise de binários (APK/IPA) e na integridade da comunicação cliente-servidor, explorando vulnerabilidades que surgem quando o desenvolvedor confia excessivamente na proteção do sistema operacional.

### 🇺🇸 Mobile App Security Analysis (Android/iOS)
Unlike Web applications, mobile apps reside on the user's device, making them targets for reverse engineering and real-time manipulation. This module focuses on binary analysis (APK/IPA) and client-server communication integrity, exploring vulnerabilities that arise when developers over-rely on the operating system's built-in protections.

---

## 🔍 Áreas de Pesquisa | Research Areas

Este módulo abrange as técnicas fundamentais do **OWASP Mobile Top 10**:

* **Static Analysis (SAST):** Descompilação de APKs utilizando `JADX` para identificar segredos de API hardcoded, URLs de staging expostas e chaves criptográficas embutidas no código.
* **Dynamic Analysis (DAST):** Manipulação de processos em tempo real utilizando `Frida` para realizar **SSL Pinning Bypass**, permitindo a interceptação de tráfego HTTPS criptografado.
* **Insecure Local Storage:** Investigação de dados sensíveis (tokens, PII, credenciais) armazenados de forma insegura em `SharedPreferences`, bancos de dados SQLite locais ou caches.
* **Logic Manipulation:** Uso de ferramentas como `Objection` para interagir com a memória do app, alterando fluxos de autenticação ou estados de permissão em tempo de execução.

---

## 🚀 Workflow de Auditoria | Audit Workflow

1.  **Reversed Engineering:** Descompilação e análise do arquivo `AndroidManifest.xml` e classes Java/Kotlin.
2.  **Traffic Interception:** Configuração de Proxy (Burp Suite) e bypass de proteções de rede (SSL Pinning).
3.  **Local Forensic:** Extração e análise da pasta `/data/data/com.app.package` para validar a persistência de dados.

---

## 🧪 Laboratórios de Pesquisa | Research Labs

| Lab | Descrição (PT) | Description (EN) | Status |
| :--- | :--- | :--- | :--- |
| **[lab-ssl-pinning](./lab-ssl-pinning)** | Bypass de proteção SSL via Frida Injection. | SSL Pinning bypass using Frida Injection. | 🧪 |
| **[lab-insecure-storage](./lab-insecure-storage)** | Extração de tokens de SQLite não criptografado. | Token extraction from unencrypted SQLite. | 🛠️ |
| **[lab-hardcoded-secrets](./lab-hardcoded-secrets)** | Análise estática para descoberta de API Keys. | Static analysis to find hardcoded API Keys. | ✅ |

---

## 🛠️ Toolstack de Pesquisa
* **JADX / Bytecode Viewer:** Para engenharia reversa e leitura de código-fonte descompilado.
* **Frida & Objection:** Para instrumentação dinâmica e exploração de memória.
* **Burp Suite:** Interceptação e análise de tráfego de rede móvel.
* **ADB (Android Debug Bridge):** Para comunicação e manipulação direta com o dispositivo/emulador.

---
<p align="center">
  <b>Mobile Security Research Module - Systems Security Engineering</b>
</p>
