# 🎯 OWASP Top 10 Research & Labs | Pesquisa e Laboratórios OWASP

**EN:** This module is the core of web security research. It documents my practical journey through the 10 most critical security risks to web applications. Each folder contains Proof of Concepts (PoC), bypass techniques, and remediation strategies.
**PT:** Este módulo é o núcleo da pesquisa de segurança web. Ele documenta minha jornada prática pelos 10 riscos de segurança mais críticos para aplicações web. Cada pasta contém Provas de Conceito (PoC), técnicas de bypass e estratégias de remediação.

---

## 📂 Risk Categories | Categorias de Risco

### A01:2021 - Broken Access Control (Controle de Acesso Quebrado)
* **EN:** Focus on IDOR (Insecure Direct Object Reference), Privilege Escalation, and Path Traversal.
* **PT:** Foco em IDOR, Escalada de Privilégio e Path Traversal.

### A02:2021 - Cryptographic Failures (Falhas Criptográficas)
* **EN:** Identifying sensitive data exposure, weak hashing (MD5/SHA1), and cleartext transmission (HTTP/FTP).
* **PT:** Identificação de exposição de dados sensíveis, hashes fracos e transmissão em texto claro.

### A03:2021 - Injection (Injeção)
* **EN:** Deep dive into SQLi (Error-based, Blind, Time-based), Command Injection (RCE), and XSS (Cross-Site Scripting).
* **PT:** Estudo profundo de SQLi, Injeção de Comando (RCE) e XSS.

### A04:2021 - Insecure Design (Design Inseguro)
* **EN:** Analyzing architectural flaws that cannot be fixed by simple patching.
* **PT:** Análise de falhas arquiteturais que não podem ser corrigidas por simples patches.

### A05:2021 - Security Misconfiguration (Configuração Incorreta)
* **EN:** Testing for default credentials, open S3 buckets, and verbose error messages.
* **PT:** Testes de credenciais padrão, buckets S3 abertos e mensagens de erro detalhadas.

### A06:2021 - Vulnerable and Outdated Components
* **EN:** Researching CVEs in old libraries, frameworks (Log4Shell), and CMS plugins.
* **PT:** Pesquisa de CVEs em bibliotecas antigas, frameworks e plugins de CMS.

### A07:2021 - Identification and Authentication Failures
* **EN:** Bypassing Multi-Factor Authentication (MFA), Brute-forcing, and Session Hijacking.
* **PT:** Bypass de MFA, Brute-force e Sequestro de Sessão (Session Hijacking).

### A08:2021 - Software and Data Integrity Failures
* **EN:** Exploiting insecure deserialization and untrusted CI/CD pipelines.
* **PT:** Exploração de deserialização insegura e pipelines de CI/CD não confiáveis.

### A09:2021 - Security Logging and Monitoring Failures
* **EN:** Studying how attackers hide their presence and why monitoring fails.
* **PT:** Estudo de como atacantes escondem sua presença e por que o monitoramento falha.

### A10:2021 - SSRF (Server-Side Request Forgery)
* **EN:** Exploiting servers to make internal requests to the infrastructure (Cloud metadata, internal APIs).
* **PT:** Exploração de servidores para realizar requisições internas (metadados de Cloud, APIs internas).

---

## 🛠️ Methodology | Metodologia
1. **Discovery:** Manual mapping and automated fuzzing.
2. **Exploitation:** Developing a clean PoC to demonstrate business impact.
3. **Mitigation:** Documenting the secure code fix for the identified flaw.

---
<p align="center">
  <b>Focus: Bug Bounty & Freelance High-Performance Auditing</b>
</p>
