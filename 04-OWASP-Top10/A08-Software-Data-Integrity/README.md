# A08:2021 - Falhas de Integridade de Software e Dados

**PT-BR:** Foca em suposições feitas sobre atualizações de software, dados críticos e pipelines de CI/CD sem a devida verificação de integridade.
**EN:** Focuses on making assumptions about software updates, critical data, and CI/CD pipelines without verifying integrity.

### 🧪 Vetores de Ataque:
* **Deserialização Insegura:** Executar código manipulando objetos serializados (Java, PHP, Python).
* **Canais de Atualização Inseguros:** Sequestrar fluxos de atualização automática.
* **Envenenamento de CI/CD:** Manipular pipelines de build para injetar código malicioso.

### 🛠️ Ferramentas:
* Ysoserial, GadgetProbe, Burp Deserialization Scanner.
