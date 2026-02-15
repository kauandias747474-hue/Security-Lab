# 💉 Lab: Secure Coding (SQL Injection Remediation)

### 🇧🇷 Diagnóstico: Substituição de Concatenação por Parametrização
Este laboratório apresenta um cenário clássico de SQLi onde a entrada do usuário é concatenada diretamente na query. Demonstramos o processo de remediação utilizando **Prepared Statements**, eliminando a possibilidade de manipulação da lógica SQL pelo atacante.

### 🇺🇸 Diagnostic: Replacing Concatenation with Parameterization
This lab presents a classic SQLi scenario where user input is directly concatenated into the query. We demonstrate the remediation process using **Prepared Statements**, eliminating the possibility of SQL logic manipulation by the attacker.



## 🛠️ Conteúdo do Lab
* `vulnerable.php / .js`: Código aceitando injeção.
* `secure.php / .js`: Código refatorado com Prepared Statements.
* `explanation.md`: Por que a parametrização é a defesa definitiva contra SQLi.
