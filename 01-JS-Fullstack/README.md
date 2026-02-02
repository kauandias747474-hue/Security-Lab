# 🌐 JavaScript & Fullstack Security | Segurança em JS e Fullstack

**EN:** JavaScript is the language of the web, but its flexible nature creates unique attack vectors. This module focuses on both Client-side and Server-side (Node.js) security.
**PT:** O JavaScript é a linguagem da web, mas sua natureza flexível cria vetores de ataque únicos. Este módulo foca tanto na segurança Client-side quanto Server-side (Node.js).

---

### 🔍 Research Areas | Áreas de Pesquisa:

#### 1. Prototype Pollution (Node.js)
* **EN:** Studying how to manipulate the `__proto__` object to inject properties into the global scope, leading to RCE (Remote Code Execution) or logic bypass.
* **PT:** Estudo de como manipular o objeto `__proto__` para injetar propriedades no escopo global, levando a RCE ou bypass de lógica.

#### 2. Advanced XSS (Cross-Site Scripting)
* **EN:** Beyond simple `alert(1)`. Researching DOM-based XSS, Bypassing CSP (Content Security Policy), and exfiltrating cookies/session tokens.
* **PT:** Além do simples `alert(1)`. Pesquisa de XSS baseado em DOM, Bypass de CSP e exfiltração de cookies/tokens de sessão.

#### 3. Insecure postMessage
* **EN:** Exploiting misconfigured Cross-Origin Communication to steal data or trigger actions on behalf of the user.
* **PT:** Exploração de comunicação Cross-Origin mal configurada para roubar dados ou disparar ações em nome do usuário.

#### 4. Node.js Hardening
* **EN:** Secure handling of `child_process`, preventing Command Injection, and auditing npm packages for supply chain attacks.
* **PT:** Manipulação segura de `child_process`, prevenção de Injeção de Comando e auditoria de pacotes npm contra ataques de Supply Chain.

---

### 🛠️ Toolstack:
* **Node.js:** For building and testing vulnerable environments.
* **Burp Suite:** DOM Invader and Proxy for traffic analysis.
* **npm audit:** For identifying known vulnerabilities in dependencies.
* **Browser DevTools:** For deep DOM and script debugging.

---

### 📖 How to study this module | Como estudar este módulo:
**EN:** Each subfolder contains a proof-of-concept (PoC) and a `mitigation.js` file showing the secure way to code the same feature.
**PT:** Cada subpasta contém uma prova de conceito (PoC) e um arquivo `mitigation.js` mostrando a forma segura de programar a mesma funcionalidade.
