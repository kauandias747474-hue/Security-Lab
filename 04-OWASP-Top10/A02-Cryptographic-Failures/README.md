# 🔐 A02:2021 - Cryptographic Failures | Laboratório de Pesquisa

### 🇧🇷 Diagnóstico de Proteção de Dados e Criptografia
Este laboratório foca na análise de falhas na proteção de dados sensíveis. A pesquisa explora como a escolha de algoritmos obsoletos, a ausência de transporte seguro (TLS) e o gerenciamento inadequado de chaves permitem que atacantes interceptem comunicações ou quebrem a confidencialidade de informações armazenadas.

### 🇺🇸 Cryptographic Failures & Data Protection Diagnostic
This lab focuses on analyzing sensitive data protection failures. The research explores how the choice of obsolete algorithms, lack of secure transport (TLS), and inadequate key management allow attackers to intercept communications or break the confidentiality of stored information.

---

## 🔬 Cenários de Pesquisa | Research Scenarios

Este módulo contém implementações práticas dos seguintes vetores de ataque e suas respectivas correções:

1. **Weak Hashing (Passwords):**
   - **Cenário:** Armazenamento de senhas utilizando algoritmos de colisão rápida como MD5 ou SHA1 sem "salting".
   - **Foco:** Demonstração de *Rainbow Tables* e ataques de dicionário em hashes legados.

2. **Cleartext Transmission (MITM):**
   - **Cenário:** Transmissão de credenciais ou dados bancários via protocolos sem criptografia (HTTP/FTP).
   - **Foco:** Simulação de *Man-in-the-Middle* (MITM) para interceptação de tráfego.

3. **Insufficient Entropy (Predictable Secrets):**
   - **Cenário:** Geração de tokens de sessão ou IDs usando `Math.random()` em vez de geradores criptograficamente seguros (CSPRNG).
   - **Foco:** Previsibilidade de sequências numéricas e sequestro de tokens.

4. **Sensitive Data Exposure (Insecure Storage):**
   - **Cenário:** Dados de PII (Informações Pessoais Identificáveis) salvos no banco de dados em texto claro ou com chaves de criptografia "hardcoded" no código.
   - **Foco:** Vazamento de dados após comprometimento de backup.

---

## 🛠️ Estrutura do Laboratório (Lab Structure)

Cada cenário dentro desta pasta está organizado da seguinte forma:

* **`vulnerable-logic.js`**: Implementação contendo falhas de hashing ou transmissão.
* **`cryptanalysis.py`**: Script de auditoria que demonstra a fragilidade da implementação (ex: quebra de hash ou interceptação).
* **`secure-implementation.js`**: Código refatorado utilizando padrões modernos (Argon2, BCrypt, Web Crypto API).

---

## 🛡️ Arquitetura de Defesa Aplicada (Remediation)

A pesquisa conclui que a mitigação eficaz de falhas A02 exige:
* **Strong Hashing:** Uso obrigatório de algoritmos adaptativos (Argon2id ou BCrypt) com fator de custo elevado.
* **HSTS & TLS 1.3:** Forçar o uso de protocolos de transporte seguro e desabilitar suites de cifra fracas.
* **CSPRNG:** Utilização da API `crypto.getRandomValues()` para qualquer valor que exija imprevisibilidade.
* **Encryption at Rest:** Criptografia de campos sensíveis no DB com AES-256-GCM.

---

### 🚀 Como Executar
1. Navegue até a subpasta do cenário desejado (ex: `01-weak-hashing`).
2. Instale as dependências: `npm install`
3. Execute o laboratório para comparar a performance e segurança entre o método legado e o moderno.

---
<p align="center">
  <b>Research Module - Systems Security Engineering</b>
</p>
