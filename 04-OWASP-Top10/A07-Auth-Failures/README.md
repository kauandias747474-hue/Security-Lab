# 🔑 A07:2021 - Identification and Authentication Failures | Falhas de Identificação e Autenticação

### 🇧🇷 Diagnóstico de Identidade, Autenticação e Gestão de Sessão
Este laboratório foca na análise de falhas críticas na confirmação da identidade do usuário e no gerenciamento de suas sessões. A pesquisa demonstra como a ausência de proteções contra ataques de força bruta, a implementação fraca de múltiplos fatores de autenticação (MFA) e a gestão insegura de identificadores de sessão permitem que atacantes realizem o sequestro de contas (Account Takeover) e comprometam a privacidade dos usuários.

### 🇺🇸 Identity, Authentication, and Session Management Diagnostic
This lab focuses on analyzing critical failures in user identity confirmation and session management. The research demonstrates how the lack of protection against brute-force attacks, weak multi-factor authentication (MFA) implementations, and insecure session identifier management allow attackers to perform account takeovers and compromise user privacy.

---

## 🔬 Cenários de Pesquisa | Research Scenarios

Este módulo contém implementações práticas e metodologias de auditoria para os seguintes vetores:

1. **Credential Stuffing & Brute Force:**
   - **🇧🇷 Cenário:** Ataques automatizados contra endpoints de login que não possuem mecanismos de bloqueio ou *Rate-Limiting*.
   - **🇺🇸 Focus:** Using leaked credential lists and automation tools (Hydra/Intruder) to gain unauthorized access.

2. **MFA Logic Bypass (Bypass de MFA):**
   - **🇧🇷 Cenário:** Exploração de falhas na lógica de verificação de dois fatores, como a possibilidade de pular a etapa de código ou reutilizar tokens expirados.
   - **🇺🇸 Focus:** Identifying architectural gaps in the second-factor authentication flow.

3. **Session Fixation & Hijacking (Sequestro de Sessão):**
   - **🇧🇷 Cenário:** Manipulação de identificadores de sessão para forçar um ID conhecido ou capturar cookies de sessão via ataques paralelos.
   - **🇺🇸 Focus:** Researching how session IDs are generated, stored, and invalidated.

4. **Weak Password Recovery (Recuperação Fraca):**
   - **🇧🇷 Cenário:** Análise de fluxos de "esqueci minha senha" que permitem a enumeração de usuários ou utilizam tokens previsíveis.
   - **🇺🇸 Focus:** Exploiting predictable password reset mechanisms and notification-based leaks.

---



## 🛠️ Ferramentas de Auditoria (Audit Toolstack)

A metodologia de pesquisa utiliza as seguintes ferramentas para diagnóstico:
* **Burp Suite Intruder:** Automação de testes de dicionário e força bruta em formulários.
* **Hydra / FFuf:** Fuzzing de alta performance para descoberta de credenciais e endpoints de autenticação.
* **OWASP ZAP:** Análise de tokens de sessão e segurança de cookies (HttpOnly, Secure, SameSite).

---

## 🛡️ Arquitetura de Defesa Aplicada (Remediation)

A pesquisa conclui que a mitigação eficaz de falhas A07 exige:

* **Adaptive Rate Limiting:** Implementação de bloqueios progressivos e CAPTCHAs após múltiplas tentativas falhas.
* **Secure Session Management:** Geração de IDs de sessão com alta entropia e invalidação total após logout ou timeout.
* **MFA Everywhere:** Implementação de autenticação multifatorial robusta (TOTP ou FIDO2) para todos os níveis de acesso sensível.
* **Password Policies:** Verificação de senhas contra listas de credenciais vazadas e exigência de complexidade mínima.

---

### 🚀 Como Executar | How to Run
1. Navegue até a subpasta do cenário (ex: `01-brute-force-lab`).
2. Inicie o servidor de autenticação: `node auth-server.js`
3. Execute o script de ataque: `python exploit-auth.py`
4. Compare com a versão protegida no arquivo `secure-auth.js` para validar a eficácia do *Rate-Limit*.

---
<p align="center">
  <b>Research Module - Systems Security Engineering</b>
</p>
