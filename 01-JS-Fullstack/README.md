# 🌐 JavaScript & Fullstack Security | Segurança em JS e Fullstack

### 🇧🇷 Engenharia Defensiva e Pesquisa de Vulnerabilidades
O JavaScript é a linguagem da web, mas sua natureza flexível cria vetores de ataque únicos. Este módulo foca na segurança de espectro completo (Fullstack), desde a manipulação do DOM no Client-side até o endurecimento (Hardening) do Runtime em Node.js.

### 🇺🇸 Fullstack Security Engineering & Vulnerability Research
JavaScript is the language of the web, but its flexible nature creates unique attack vectors. This module focuses on full-spectrum security, from Client-side DOM manipulation to Node.js Runtime Hardening.

---

### 🔍 Áreas de Pesquisa (Research Areas)

| Lab / PoC | Foco Técnico (PT/EN) | Conceito Chave / Key Concept |
| :--- | :--- | :--- |
| `prototype-pollution` | Manipulação de `__proto__` e RCE. / Proto manipulation. | **Object Integrity** |
| `advanced-xss` | Bypass de CSP e XSS baseado em DOM. / CSP Bypass. | **XSS Sanitization** |
| `postmessage-exploit` | Falhas em Cross-Origin Communication. / Origin leakage. | **Secure Messaging** |
| `node-hardening` | Prevenção de Command Injection. / Command Injection prevention. | **Runtime Hardening** |
| `supply-chain-audit` | Auditoria de dependências NPM. / NPM audit & Supply Chain. | **Dependency Security** |

---

### 🛠️ Toolstack de Auditoria
* **Runtime:** Node.js (Vulnerable environments simulation)
* **Analysis:** Burp Suite (DOM Invader), npm audit, OWASP ZAP.
* **Defense:** Snyk, Trusted Types API, Helmet.js.

---

### 📖 Estrutura do Módulo (How to Study)
> [!IMPORTANT]
> Cada subpasta contém uma **Proof of Concept (PoC)** demonstrando a falha técnica e um arquivo `mitigation.js` (ou `.ts`) mostrando a implementação segura seguindo as melhores práticas da OWASP.

---

### 👨‍💻 Autor
**Kauan Oliveira** | Fullstack Engineer (Security & Pentest Focus)
