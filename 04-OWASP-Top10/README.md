# 🎯 OWASP Top 10 Research & Labs | Pesquisa de Segurança de Sistemas

### 🇧🇷 Framework de Pesquisa e Engenharia Defensiva
Este módulo representa o núcleo da minha pesquisa em segurança de software. Ele documenta uma análise técnica profunda dos riscos mais críticos para aplicações modernas, conforme o padrão global da OWASP. Cada diretório contém **Ambientes Controlados (PoCs)**, análises de vulnerabilidades em nível de sistema e, o mais importante, **Arquiteturas de Correção** para mitigar riscos estruturais e garantir a integridade do ciclo de vida do software.

### 🇺🇸 Security Engineering & Defensive Research Framework
This module represents the core of my software security research. It documents a deep technical analysis of the most critical risks for modern applications, following the OWASP global standard. Each directory contains **Controlled Environments (PoCs)**, system-level vulnerability analysis, and, most importantly, **Remediation Architectures** to mitigate structural risks and ensure the integrity of the software development lifecycle.

---

## 📂 Taxonomia de Riscos | Risk Taxonomy

| Categoria / Category | Foco da Pesquisa / Research Focus (PT/EN) | Conceito Chave / Key Concept |
| :--- | :--- | :--- |
| **A01:2021** | **Controle de Acesso Quebrado:** IDOR, Escalada de Privilégio e Path Traversal. / Broken Access Control: IDOR, Privilege Escalation. | **Access Control Logic** |
| **A02:2021** | **Falhas Criptográficas:** Exposição de dados, hashes fracos e tráfego inseguro. / Cryptographic Failures: Weak hashing & cleartext data. | **Data-at-Rest Protection** |
| **A03:2021** | **Injeção:** SQLi (Blind/Time-based), Command Injection (RCE) e XSS Avançado. / Injection: Deep dive into SQLi, RCE and XSS. | **Input Sanitization** |
| **A04:2021** | **Design Inseguro:** Análise de falhas na arquitetura lógica e fluxos de negócio. / Insecure Design: Analysis of architectural flaws. | **Secure Architecture** |
| **A05:2021** | **Configuração Incorreta:** Endurecimento de servidores e segurança de nuvem. / Security Misconfiguration: Server hardening & cloud security. | **Hardening Protocols** |
| **A06:2021** | **Componentes Vulneráveis:** Análise de CVEs e Auditoria de Supply Chain. / Vulnerable Components: CVE research & Supply Chain auditing. | **Dependency Integrity** |
| **A07:2021** | **Falhas de Identificação:** Vulnerabilidades em MFA, Gestão de Sessão e Auth. / Identification Failures: MFA Bypass & Session Management. | **Identity Management** |
| **A08:2021** | **Integridade de Software:** Desserialização insegura e segurança em CI/CD. / Software Integrity: Insecure deserialization & CI/CD security. | **Pipeline Security** |
| **A09:2021** | **Falhas de Monitoramento:** Diagnóstico de visibilidade e integridade de Logs. / Monitoring Failures: Visibility diagnostics & Log integrity. | **Observability & Logs** |
| **A10:2021** | **SSRF:** Falsificação de requisição do lado do servidor e Metadados Cloud. / SSRF: Server-Side Request Forgery & Cloud Metadata. | **Server Trust Models** |

---

## 🛠️ Metodologia de Engenharia (Engineering Methodology)

Para cada laboratório desenvolvido neste módulo, é aplicado um rigoroso protocolo de auditoria e engenharia:

1.  **Environment Setup (Reprodução):** Criação de um ambiente isolado (Node.js/Docker) que emula fielmente a vulnerabilidade.
2.  **Vulnerability Analysis (Análise):** Documentação técnica de como a falha ocorre no nível da memória, do motor de execução (V8) ou do protocolo de rede.
3.  **Remediation & Hardening (Blindagem):** Implementação da solução definitiva utilizando princípios de **Zero Trust**, **Secure Coding** e arquitetura defensiva.

---

## 🚀 Diferencial Profissional (Professional Edge)

> [!IMPORTANT]
> **Security-by-Design:** Minha pesquisa não foca apenas na exploração técnica, mas na **prevenção estratégica**. Este laboratório demonstra maturidade para atuar em projetos de alta complexidade onde a segurança é tratada como um requisito não-funcional prioritário, protegendo o negócio contra vetores de ataque modernos.

---

### 👨‍💻 Autor
**Kauan Oliveira** | Software Engineer & Security Researcher
