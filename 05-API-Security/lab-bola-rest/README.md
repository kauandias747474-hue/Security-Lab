# 🏥 Lab: BOLA (Broken Object Level Authorization)

### 🇧🇷 Diagnóstico: Autorização de Nível de Objeto
O **BOLA** ocorre quando a API não verifica se o usuário autenticado tem permissão para acessar um objeto específico através de seu ID. Neste cenário, simulamos um sistema de prontuários médicos onde um usuário autenticado consegue ler dados de outros pacientes apenas alterando o ID na URL.

### 🇺🇸 Diagnostic: Broken Object Level Authorization
**BOLA** occurs when the API fails to verify if the authenticated user has permission to access a specific object via its ID. In this scenario, we simulate a medical record system where an authenticated user can read other patients' data just by changing the ID in the URL.

---

## 🔬 O Ataque | The Attack
1. O atacante faz login e recebe um token JWT válido.
2. O atacante acessa seu próprio prontuário em `GET /api/v1/records/101`.
3. O atacante altera o ID para `GET /api/v1/records/102` e acessa dados de terceiros.



## 🛠️ Estrutura do Lab
* `vulnerable-api.js`: Servidor Express que valida o token, mas ignora a propriedade do recurso.
* `exploit-poc.py`: Script que automatiza a extração de dados sensíveis via Insecure ID.
* `secure-api.js`: Versão corrigida com check de **Ownership Permission**.

## 🛡️ Mitigação
* Implementação de uma camada de autorização que cruza o `user_id` do token com o `owner_id` do recurso no banco de dados.
* Uso de **UUIDs** para dificultar a enumeração de IDs.

---
