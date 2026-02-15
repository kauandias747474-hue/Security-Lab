# 🧬 Lab: SSTI (Server-Side Template Injection)

### 🇧🇷 Diagnóstico: Identificação de Motores de Template
A Injeção de Template no Lado do Servidor (SSTI) ocorre quando o input do usuário é concatenado em um template antes da renderização. Este laboratório organiza payloads para realizar o "fingerprinting" preciso de motores como **Jinja2, Mako, Thymeleaf e Twig** através de respostas diferenciais a operações matemáticas.

### 🇺🇸 Diagnostic: Template Engine Identification
Server-Side Template Injection (SSTI) occurs when user input is concatenated into a template before rendering. This lab organizes payloads to perform precise fingerprinting of engines such as **Jinja2, Mako, Thymeleaf, and Twig** through differential responses to mathematical operations.

---

## 🛡️ Mitigação | Remediation

* **Context-Aware Escaping:** Garantir que o motor de template trate todo input como dado, não como código.
* **Sandboxing:** Executar a renderização em ambientes restritos (low-privilege).
* **Input Validation:** Bloquear sintaxes de template como `{{`, `${` ou `{%`.



## 🛠️ Conteúdo do Lab | Lab Content
* `ssti-polyglots.txt`: Strings de teste universais para detecção rápida de motores.
* `engine-payloads.py`: Scripts específicos para exploração de RCE em cada tecnologia.

---
