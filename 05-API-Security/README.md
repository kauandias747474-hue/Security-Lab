# 🔌 API Security & Logic Audits

As APIs são a espinha dorsal das aplicações modernas e um dos alvos mais rentáveis em Bug Bounty. Este módulo foca especificamente em protocolos REST, GraphQL e gRPC.

## 🔍 Áreas de Pesquisa
* **BOLA (Broken Object Level Authorization):** A falha número 1 em APIs, onde um usuário acessa dados de outro via manipulação de IDs.
* **Mass Assignment:** Injeção de parâmetros não previstos para alterar estados do servidor (ex: virar `admin: true`).
* **GraphQL Attacks:** Abuso de introspecção, ataques de negação de serviço (DoS) via queries complexas e vazamento de esquema.
* **Improper Assets Management:** Descoberta de APIs de sombra (Shadow APIs) e versões antigas (V1 vs V2) expostas.

## 🚀 Workflow de Teste
1. **Mapeamento:** Documentação da API (Swagger/Postman).
2. **Fuzzing:** Teste de verbos HTTP (GET, POST, PUT, DELETE, PATCH).
3. **Lógica:** Teste de fluxo de negócio e controle de acesso aos recursos.

## 🛠️ Ferramentas Utilizadas
* **Postman:** Testes manuais e automação de coleções.
* **Kiterunner:** Scan de endpoints de API.
* **Graphw00f:** Fingerprinting de servidores GraphQL.
