# 💉 A03:2021 - Injection | Laboratório de Pesquisa

### 🇧🇷 Diagnóstico de Injeção e Integridade de Comandos
Este laboratório foca na análise de falhas onde dados não confiáveis são inseridos em interpretadores, sendo executados como comandos legítimos. A pesquisa demonstra como a falta de sanitização permite que atacantes subvertam a lógica de consultas a bancos de dados, executem comandos no sistema operacional ou injetem scripts maliciosos no navegador de outros usuários.

### 🇺🇸 Injection & Command Integrity Diagnostic
This lab focuses on analyzing flaws where untrusted data is sent to interpreters and executed as part of a command or query. The research demonstrates how lack of sanitization allows attackers to subvert database logic, execute OS-level commands, or inject malicious scripts into other users' browsers.

---

## 🔬 Cenários de Pesquisa | Research Scenarios

Este módulo contém implementações práticas dos seguintes vetores de ataque e suas respectivas correções:

1. **SQL Injection (SQLi):**
   - **🇧🇷 Cenário:** Manipulação de queries via parâmetros de URL ou corpos de requisição (Ex: `' OR 1=1 --`).
   - **🇺🇸 Focus:** Error-based, Union-based, and Blind SQLi (Time-based) techniques.

2. **Command Injection (RCE):**
   - **🇧🇷 Cenário:** Passagem de argumentos para funções do sistema (como `child_process.exec`) sem validação.
   - **🇺🇸 Focus:** Remote Code Execution (RCE) and lateral movement within the server.

3. **Cross-Site Scripting (XSS):**
   - **🇧🇷 Cenário:** Injeção de scripts maliciosos que são refletidos no DOM ou armazenados permanentemente.
   - **🇺🇸 Focus:** Stored, Reflected, and DOM-based XSS, including cookie exfiltration techniques.

4. **NoSQL Injection:**
   - **🇧🇷 Cenário:** Exploração de filtros em bancos não-relacionais (como MongoDB) através de objetos de consulta (Ex: `{$gt: ""}`).
   - **🇺🇸 Focus:** Authentication bypass in NoSQL environments.

---



## 🛠️ Estrutura do Laboratório (Lab Structure)

Cada cenário dentro desta pasta está organizado da seguinte forma:

* **`vulnerable-service.js`**: Implementação contendo interpretadores expostos a dados não tratados.
* **`exploit-payload.py`**: Gerador de payloads para demonstrar a quebra da lógica original do sistema.
* **`secure-pattern.js`**: Código refatorado utilizando consultas parametrizadas e APIs seguras.

---

## 🛡️ Arquitetura de Defesa Aplicada (Remediation)

A pesquisa conclui que a mitigação eficaz de falhas A03 exige:

* **Parameterized Queries:** Uso obrigatório de *Prepared Statements* em qualquer interação com banco de dados.
* **Input Validation (Allow-listing):** Validação rigorosa de tipos, tamanhos e formatos (Regex) antes do processamento.
* **Output Encoding:** Codificação de dados antes de renderizá-los no navegador para neutralizar scripts maliciosos.
* **Safe APIs:** Substituição de funções perigosas (como `eval()` ou `exec()`) por alternativas que não invocam o shell do sistema.

---

### 🚀 Como Executar | How to Run
1. Navegue até a subpasta do cenário (ex: `01-sqli-research`).
2. Instale as dependências: `npm install`
3. Inicie o ambiente: `node vulnerable-service.js`
4. Execute o script de exploit para observar a interceptação ou alteração da lógica.

---
<p align="center">
  <b>Research Module - Systems Security Engineering</b>
</p>
