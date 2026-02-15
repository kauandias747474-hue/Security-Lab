# 🔌 API Security & Logic Audits | Auditoria de Lógica e Segurança de APIs

### 🇧🇷 Engenharia de Segurança em APIs e Microsserviços
As APIs são a espinha dorsal da arquitetura de software moderna. Este módulo é dedicado à pesquisa de vulnerabilidades em protocolos **REST, GraphQL e gRPC**, focando não apenas na exploração, mas na implementação de mecanismos de defesa robustos como API Gateways, validação de esquemas e políticas de autorização granular para proteger o ecossistema de microsserviços.

### 🇺🇸 API Security Engineering & Microservices Audit
APIs are the backbone of modern software architecture. This module is dedicated to researching vulnerabilities in **REST, GraphQL, and gRPC** protocols, focusing not only on exploitation but also on implementing robust defense mechanisms such as API Gateways, schema validation, and granular authorization policies to protect the microservices ecosystem.

---

## 🔍 Áreas de Pesquisa | Research Areas

Este módulo explora as categorias mais críticas do **OWASP API Security Top 10**:

* **BOLA (Broken Object Level Authorization):** Pesquisa sobre falhas de autorização onde a validação de propriedade do recurso é insuficiente, permitindo acesso a dados de terceiros via manipulação de IDs.
* **Mass Assignment & Type Juggling:** Injeção de parâmetros não previstos para manipulação de estado do servidor e escalada de privilégios (ex: `isAdmin: true`).
* **GraphQL Security:** Análise de abusos de introspecção, circularidade de consultas (DoS por profundidade) e exfiltração de esquemas.
* **Improper Assets Management:** Identificação de *Shadow APIs*, versões legadas expostas (v1 vs v2) e documentação de endpoints (Swagger/OAS) insegura.

---

## 🧪 Laboratórios de Pesquisa | Research Labs

| Lab | Descrição (PT) | Description (EN) | Status |
| :--- | :--- | :--- | :--- |
| **[lab-bola-rest](./lab-bola-rest)** | Bypass de autorização em sistema multi-tenant. | Authorization bypass in multi-tenant systems. | 🛠️ |
| **[lab-mass-assignment](./lab-mass-assignment)** | Escala de privilégio via poluição de parâmetros. | Privilege escalation via parameter pollution. | 🛠️ |
| **[lab-graphql-dos](./lab-graphql-dos)** | Exaustão de recursos via consultas recursivas. | Resource exhaustion via recursive queries. | 🧪 |
| **[lab-shadow-api](./lab-shadow-api)** | Exploração de endpoints v1/v2 depreciados. | Exploiting deprecated v1/v2 endpoints. | 🧪 |

---

## 🚀 Workflow de Auditoria | Audit Workflow

O processo de auditoria neste repositório segue três pilares fundamentais:

1.  **Recon & Mapping:** Descoberta ativa e passiva de endpoints, análise de documentação (Swagger/OAS) e testes de introspecção GraphQL.
2.  **Schema Validation:** Testes de estresse em contratos de dados, checagem de tipos e suporte a verbos HTTP (GET, POST, PUT, DELETE, PATCH).
3.  **Logic & Authorization:** Verificação de fluxos de negócio complexos e validação de propriedade de recursos (*Ownership Validation*).

---

## 🛡️ Defesa Aplicada | Applied Defense

A mitigação das falhas encontradas nestes laboratórios foca em:
* **Implementação de DTOs (Data Transfer Objects):** Para evitar Mass Assignment e vazamento de campos internos.
* **Middleware de Autorização:** Para validação rigorosa de propriedade (Ownership) baseada no contexto do JWT.
* **Query Depth Limiting:** Para proteção de infraestrutura contra consultas GraphQL abusivas.
* **API Gateway Hardening:** Gerenciamento centralizado de versões e controle de ativos.

---

## 🛠️ Toolstack de Pesquisa
* **Postman / Insomnia:** Automação de testes de contrato e suites de regressão.
* **Kiterunner:** Descoberta de ativos e mapeamento de rotas de API em alta performance.
* **Graphw00f / Clairvoyance:** Auditoria, fingerprinting e reconstrução de esquemas GraphQL.
* **Zod / Joi:** Bibliotecas de validação de esquema utilizadas nas mitigações.

---
<p align="center">
  <b>Research Module - Systems Security Engineering</b>
</p>
