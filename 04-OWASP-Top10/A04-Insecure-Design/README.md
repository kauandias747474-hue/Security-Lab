# 🏛️ A04:2021 - Insecure Design | Laboratório de Pesquisa

### 🇧🇷 Diagnóstico de Falhas de Design e Arquitetura
Este laboratório foca na análise de falhas estruturais que ocorrem antes mesmo da implementação do código. A pesquisa demonstra como decisões de design inadequadas — como fluxos de negócio sem limites de uso, processos de recuperação de credenciais previsíveis ou falta de segregação de funções — criam vulnerabilidades que não podem ser corrigidas apenas com "patches" técnicos, exigindo uma reestruturação da lógica do sistema.

### 🇺🇸 Insecure Design & Architectural Failures Diagnostic
This lab focuses on analyzing structural flaws that occur even before code implementation. The research demonstrates how inadequate design decisions — such as business logic flows without rate limits, insecure credential recovery processes, or lack of segregation of duties — create vulnerabilities that cannot be fixed by simple technical patches, requiring a restructuring of the system's logic.

---

## 🔬 Cenários de Pesquisa | Research Scenarios

Este módulo contém implementações práticas dos seguintes vetores de falha e suas respectivas correções:

1. **Business Logic Bypass (Burla de Lógica de Negócio):**
   - **🇧🇷 Cenário:** Manipulação de fluxos de e-commerce onde é possível enviar quantidades negativas ou preços customizados via payload.
   - **🇺🇸 Focus:** Server-side enforcement of business rules and price integrity.

2. **Insecure Password Recovery (Recuperação de Senha Insegura):**
   - **🇧🇷 Cenário:** Fluxos de "esqueci minha senha" que utilizam perguntas de segurança fáceis de pesquisar ou tokens previsíveis.
   - **🇺🇸 Focus:** Implementation of unique, time-bound, and high-entropy reset tokens.

3. **Rate Limiting & Resource Exhaustion (Exaustão de Recursos):**
   - **🇧🇷 Cenário:** Endpoints de geração de relatórios ou PDFs que permitem requisições infinitas, levando à negação de serviço (DoS).
   - **🇺🇸 Focus:** Implementation of Throttling, Quotas, and Resource Management.

4. **Trusting Client-Side Integrity (Confiança no Cliente):**
   - **🇧🇷 Cenário:** Sistemas que confiam no Front-end para calcular descontos ou validar permissões de UI.
   - **🇺🇸 Focus:** Zero-trust architecture where the server validates every step of the transaction.

---



## 🛠️ Estrutura do Laboratório (Lab Structure)

Cada cenário dentro desta pasta está organizado da seguinte forma:

* **`design-flaw-demo.js`**: Implementação de um fluxo de negócio funcional, porém estruturalmente vulnerável.
* **`logic-exploit.py`**: Script que demonstra como a falha de design permite ganho indevido ou bypass de regras.
* **`secure-architecture.js`**: Refatoração do fluxo aplicando princípios de "Secure-by-Design" e validações atômicas no servidor.

---

## 🛡️ Arquitetura de Defesa Aplicada (Remediation)

A pesquisa conclui que a mitigação eficaz de falhas A04 exige:

* **Threat Modeling:** Realização de modelagem de ameaças durante a fase de desenho da solução.
* **Server-Side Truth:** O servidor deve ser a única fonte da verdade para preços, permissões e estados de fluxo.
* **Principle of Least Privilege:** O sistema deve ser desenhado para que falhas em um componente não comprometam toda a lógica de negócio.
* **Cyclomatic Complexity Control:** Manter a lógica simples e auditável para evitar estados imprevistos que possam ser explorados.

---

### 🚀 Como Executar | How to Run
1. Navegue até a subpasta do cenário (ex: `01-logic-flaws`).
2. Instale as dependências: `npm install`
3. Inicie o laboratório: `node design-flaw-demo.js`
4. Use o script de exploração para testar os limites e falhas da lógica implementada.

---
<p align="center">
  <b>Research Module - Systems Security Engineering</b>
</p>
