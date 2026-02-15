# 🔓 A01:2021 - Broken Access Control | Laboratório de Pesquisa

### 🇧🇷 Diagnóstico de Controle de Acesso e Autorização
Este laboratório foca na análise de falhas onde as políticas de controle de acesso não são aplicadas de forma rigorosa no lado do servidor. A pesquisa demonstra como a confiança excessiva em parâmetros fornecidos pelo cliente permite que usuários subvertam a lógica de negócio para acessar, modificar ou deletar dados de terceiros.

### 🇺🇸 Access Control & Authorization Diagnostic
This lab focuses on analyzing flaws where access control policies are not strictly enforced on the server side. The research demonstrates how over-reliance on client-side parameters allows users to subvert business logic to access, modify, or delete third-party data.

---

## 🔬 Cenários de Pesquisa | Research Scenarios

Este módulo contém implementações práticas dos seguintes vetores de ataque e suas respectivas correções:

1. **IDOR (Insecure Direct Object Reference):**
   - **Cenário:** Enumeração de IDs de documentos sensíveis via manipulação de parâmetros em rotas REST.
   - **Foco:** Diferença entre Autenticação (Quem você é) e Autorização (O que você pode fazer).

2. **Privilege Escalation (Mass Assignment):**
   - **Cenário:** Injeção de propriedades administrativas (`isAdmin: true`) em payloads de atualização de perfil.
   - **Foco:** Validação de esquemas de entrada (Input Schema Validation).

3. **CORS Misconfiguration:**
   - **Cenário:** Configuração permissiva de `Access-Control-Allow-Origin` permitindo vazamento de dados para origens não confiáveis.
   - **Foco:** Segurança de comunicação entre domínios.

4. **Path Traversal / Forced Browsing:**
   - **Cenário:** Acesso a arquivos de configuração do sistema (`.env`, `config.json`) através de rotas de entrega de arquivos estáticos.
   - **Foco:** Hardening de servidores de arquivos e filtros de caminho.

---

## 🛠️ Estrutura do Laboratório (Lab Structure)

Cada cenário dentro desta pasta está organizado da seguinte forma:

* **`vulnerable-api.js`**: Implementação em Node.js contendo a falha lógica estrutural.
* **`exploit-poc.py`**: Script de automação que demonstra a exploração da vulnerabilidade.
* **`mitigation.js`**: Código refatorado aplicando padrões de segurança (ex: RBAC, UUIDs, Middleware de Propriedade).

---

## 🛡️ Arquitetura de Defesa Aplicada (Remediation)

A pesquisa conclui que a mitigação eficaz de falhas A01 exige:
* **Deny by Default:** Bloqueio de todos os recursos, permitindo acesso apenas via regras explícitas.
* **Ownership Validation:** Verificação obrigatória de se o recurso solicitado pertence ao `user_id` da sessão ativa.
* **Opaque Tokens:** Uso de identificadores não previsíveis (UUID v4) para evitar ataques de enumeração.

---

### 🚀 Como Executar
1. Navegue até a subpasta do cenário desejado.
2. Instale as dependências: `npm install`
3. Inicie o ambiente vulnerável: `node vulnerable-api.js`
4. Execute o script de prova de conceito em um terminal separado para validar a falha.

---
<p align="center">
  <b>Research Module - Systems Security Engineering</b>
</p>
