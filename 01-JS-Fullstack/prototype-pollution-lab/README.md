# 🧬 Prototype Pollution Lab | Node.js Security

### 🇧🇷 Poluição de Protótipo e Injeção Global
Pesquisa sobre como o uso inadequado de funções de cópia profunda (*Deep Merge*) pode permitir que um atacante polua o `Object.prototype`, levando a desvios de lógica ou Execução Remota de Código (RCE).
* **Mitigação:** Uso de `Object.create(null)` e congelamento de protótipos.

---

### 🇺🇸 Prototype Pollution & Global Injection
Research on how improper use of Deep Merge functions can allow an attacker to pollute `Object.prototype`, leading to logic bypass or Remote Code Execution (RCE).
* **Mitigation:** Using `Object.create(null)` and prototype freezing.
