# 🔌 API Security & Logic Audits | Auditoria de Lógica e Segurança de APIs

### 🇧🇷 Engenharia de Segurança em APIs e Microsserviços
As APIs são a espinha dorsal da arquitetura de software moderna. Este módulo é dedicado à pesquisa de vulnerabilidades em protocolos REST, GraphQL e gRPC, focando não apenas na exploração, mas na implementação de mecanismos de defesa robustos como gateways de API, validação de esquemas e políticas de autorização granular.

### 🇺🇸 API Security Engineering & Microservices Audit
APIs are the backbone of modern software architecture. This module is dedicated to researching vulnerabilities in REST, GraphQL, and gRPC protocols, focusing not only on exploitation but also on implementing robust defense mechanisms such as API gateways, schema validation, and granular authorization policies.

---

## 🔍 Áreas de Pesquisa | Research Areas

* **BOLA (Broken Object Level Authorization):** Pesquisa sobre falhas de autorização onde a validação de propriedade do recurso é inexistente ou insuficiente.
* **Mass Assignment & Type Juggling:** Injeção de parâmetros para manipulação de estado do servidor e escalada de privilégios.
* **GraphQL Security:** Análise de ataques de introspecção, circularidade de consultas (DoS) e exposição de esquemas.
* **Improper Assets Management:** Identificação de Shadow APIs, versões legadas expostas e documentação de endpoints (Swagger/OAS) insegura.

---



## 🚀 Workflow de Auditoria | Audit Workflow

1.  **Recon & Mapping:** Descoberta de endpoints e documentação via Swagger/Postman/Introspection.
2.  **Schema Validation:** Testes de integridade de dados e tipos em verbos HTTP (GET, POST, PUT, DELETE, PATCH).
3.  **Logic & Authorization:** Verificação de fluxos de negócio e controle de acesso baseado em contexto.

---

## 🛠️ Toolstack de Pesquisa
* **Postman/Insomnia:** Automação de testes de contrato e suites de regressão.
* **Kiterunner:** Descoberta de ativos e mapeamento de rotas.
* **Graphw00f / Clairvoyance:** Auditoria e fingerprinting de infraestrutura GraphQL.

---
<p align="center">
  <b>API Security Research Module</b>
</p>
