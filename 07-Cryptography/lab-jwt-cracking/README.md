# 🎫 Lab: JWT (JSON Web Token) Security Auditing

### 🇧🇷 Cenário: Manipulação de Tokens de Sessão
O JWT é amplamente usado para autenticação. Este lab demonstra dois ataques comuns: a alteração do cabeçalho para `alg: none` (ignorando a assinatura) e o ataque de força bruta contra o segredo HMAC quando este é curto ou baseado em palavras de dicionário.

### 🇺🇸 Scenario: Session Token Manipulation
JWT is widely used for authentication. This lab demonstrates two common attacks: changing the header to `alg: none` (bypassing signature) and brute-forcing the HMAC secret when it is short or dictionary-based.



## 🛠️ Conteúdo
* `jwt-bruteforce.py`: Script para testar segredos comuns em tokens capturados.
* `none-algorithm-bypass.js`: PoC para forjar tokens de administrador sem assinatura.
