# 🔐 Cryptography Research | Pesquisa em Criptografia

### 🇧🇷 Análise de Implementações Criptográficas
Criptografia mal implementada é o mesmo que nenhuma criptografia. Este laboratório estuda a diferença entre algoritmos robustos e implementações falhas. O foco recai sobre a identificação de cifras obsoletas, o abuso de configurações de tokens (JWT) e a quebra de hashes por força bruta, demonstrando por que a escolha de algoritmos modernos e a gestão de chaves são vitais.

### 🇺🇸 Cryptographic Implementation Analysis
Badly implemented cryptography is the same as no cryptography. This lab studies the gap between robust algorithms and flawed implementations. The focus lies on identifying obsolete ciphers, abusing token configurations (JWT), and cracking hashes via brute force, demonstrating why choosing modern algorithms and proper key management is vital.

---

## 🔍 Áreas de Pesquisa | Research Areas

* **JWT (JSON Web Tokens):** Pesquisa sobre ataques de confusão de algoritmo (ex: "none" alg) e ataques de força bruta contra chaves secretas fracas (HMAC).
* **Hash Analysis & Cracking:** Estudo de colisões em MD5/SHA1 e técnicas de quebra de hashes SHA256/Bcrypt usando wordlists customizadas e regras de mutação.
* **Hardcoded Keys & Secrets:** Localização de chaves mestras e sementes (seeds) criptográficas dentro de binários ou código-fonte.
* **Insecure Randomness:** Investigação de geradores de números pseudo-aleatórios (PRNG) previsíveis que comprometem chaves de sessão.

---

## 🧪 Laboratórios de Pesquisa | Research Labs

| Lab | Descrição (PT) | Description (EN) | Status |
| :--- | :--- | :--- | :--- |
| **[lab-jwt-cracking](./lab-jwt-cracking)** | Quebra de segredos JWT e ataque de algoritmo "none". | JWT secret cracking and "none" algorithm attack. | ✅ |
| **[lab-hash-cracking](./lab-hash-cracking)** | Recuperação de senhas via Hashcat e regras complexas. | Password recovery via Hashcat and complex rules. | 🧪 |
| **[lab-insecure-ciphers](./lab-insecure-ciphers)** | Exploração de protocolos usando RC4 ou DES. | Exploiting protocols using RC4 or DES. | 🛠️ |

---

## 🛠️ Toolstack de Pesquisa
* **Hashcat / John the Ripper:** Ferramentas líderes para quebra de hashes via GPU/CPU.
* **JWT.io / PyJWT:** Manipulação e inspeção de tokens JWT.
* **CyberChef:** A "canivete suíço" para decodificação, conversão e análise de dados criptográficos.
* **Entropy Checkers:** Ferramentas para medir a aleatoriedade de chaves e arquivos.

---
<p align="center">
  <b>Cryptography Research Module - Systems Security Engineering</b>
</p>
