# 🛡️ Defensive Hardening (Blue Team) | Endurecimento Defensivo

### 🇧🇷 Estratégias de Remediação e Defesa Ativa
Para ser um bom atacante, é fundamental saber como as defesas são construídas. Este módulo é dedicado à engenharia defensiva, focando em transformar vulnerabilidades identificadas em código seguro e infraestrutura resiliente. Pesquisamos a aplicação de patches, o endurecimento de servidores (Hardening) e a configuração de camadas de proteção perimetral como WAFs, garantindo que a segurança seja aplicada desde o desenvolvimento (Secure SDLC) até a operação.

### 🇺🇸 Remediation Strategies and Active Defense
To be a good attacker, you must know how defenses are built. This module is dedicated to defensive engineering, focusing on transforming identified vulnerabilities into secure code and resilient infrastructure. We research patch application, server hardening, and the configuration of perimeter protection layers like WAFs, ensuring security is applied from development (Secure SDLC) to operations.

---

## 🔍 Áreas de Pesquisa | Research Areas

* **Code Remediation (Refactoring):** Exemplos práticos de "Antes" (vulnerável) e "Depois" (seguro) para falhas críticas como SQL Injection, XSS e IDOR.
* **WAF Hardening:** Configuração avançada de regras em **Cloudflare** ou **ModSecurity** para bloqueio preventivo de ataques automatizados.
* **Server Hardening:** Guia de boas práticas para blindagem de servidores (SSH, desativação de serviços desnecessários e permissões de sistema).
* **Security Headers:** Implementação de políticas de segurança via HTTP Headers (CSP, HSTS, X-Frame-Options) para mitigar ataques client-side.

---



## 🧪 Laboratórios de Defesa | Defense Labs

| Lab | Descrição (PT) | Description (EN) | Status |
| :--- | :--- | :--- | :--- |
| **[lab-secure-coding-sqli](./lab-secure-coding-sqli)** | Refatoração de queries SQL para Prepared Statements. | Refactoring SQL queries to Prepared Statements. | ✅ |
| **[lab-waf-rules](./lab-waf-rules)** | Criação de regras customizadas para ModSecurity. | Creating custom rules for ModSecurity. | 🧪 |
| **[lab-header-hardening](./lab-header-hardening)** | Configuração de headers de segurança globais. | Global security headers configuration. | 🛠️ |

---

## 🛠️ Toolstack
* **Cloudflare / ModSecurity:** Web Application Firewalls.
* **OWASP Coreruleset (CRS):** Conjunto de regras padrão para WAF.
* **SonarQube / Snyk:** Ferramentas de análise estática de código (SAST).
* **Linux Hardening Scripts:** Scripts para automação de segurança em SO.

---
<p align="center">
  <b>Blue Team & Remediation Module - Systems Security Engineering</b>
</p>
