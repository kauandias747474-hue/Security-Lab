# 👻 Lab: Shadow API (Improper Assets Management)

### 🇧🇷 Diagnóstico: Endpoints Depreciados e APIs de Sombra
Este laboratório foca na falha de gestão de ativos (Asset Management). O risco ocorre quando uma nova versão da API (`v2`) é lançada com correções de segurança e novas funcionalidades, mas a versão antiga (`v1`) continua ativa e acessível no servidor. Atacantes utilizam técnicas de *Fuzzing* para encontrar esses endpoints esquecidos e explorar vulnerabilidades que já haviam sido corrigidas na versão atual.

### 🇺🇸 Diagnostic: Shadow API & Deprecated Endpoints
This lab focuses on improper asset management. The risk occurs when a new API version (`v2`) is launched with security patches and new features, but the legacy version (`v1`) remains active and reachable on the server. Attackers use *Fuzzing* techniques to find these forgotten endpoints and exploit vulnerabilities that had already been patched in the current version.

---

## 🔬 O Ataque | The Attack

1.  **Reconhecimento:** O atacante observa que a aplicação oficial usa a rota `POST /api/v2/login`, que possui proteção de MFA e Rate Limiting.
2.  **Fuzzing de Diretórios:** Usando ferramentas como `Kiterunner` ou `ffuf`, o atacante descobre que a rota `POST /api/v1/login` ainda responde às requisições.
3.  **Exploração:** A versão `v1` é vulnerável a **NoSQL Injection** ou não possui **Rate Limiting**, permitindo um ataque de força bruta bem-sucedido para comprometer contas.



## 🛠️ Estrutura do Lab

Este laboratório contém um ambiente simulado com:
* **`dual-stack-server.js`**: Um servidor Express que levanta dois roteadores. O roteador `v2` é seguro (hardened), enquanto o `v1` (Shadow) contém falhas lógicas propositais.
* **`kiterunner-scan.sh`**: Script para simular a descoberta de endpoints não documentados.
* **`shadow-exploit.py`**: Exploit focado em abusar da falta de limites na versão depreciada.

---

## 🛡️ Mitigação | Remediation

A pesquisa neste laboratório demonstra as seguintes defesas:

* **Sunset Policy:** Implementação de cabeçalhos HTTP `Deprecation` e `Sunset`, seguidos pelo desligamento total de versões antigas.
* **API Gateway Routing:** Configuração de gateways (como Kong ou Nginx) para rotear apenas versões explicitamente permitidas.
* **Inventory & Audit:** Auditorias periódicas de rotas para garantir que a documentação (Swagger/OAS) reflete exatamente o que está rodando em produção.
* **In-depth Defense:** Aplicação de patches de segurança de forma retroativa (backporting) se uma versão antiga precisar ser mantida por compatibilidade.

---

## 🚀 Como Executar | How to Run

1. Instale as dependências: `npm install`
2. Inicie o servidor: `node dual-stack-server.js`
3. Execute o fuzzer para descobrir a Shadow API: `./kiterunner-scan.sh`
4. Teste o exploit na rota `/api/v1/` e compare com o bloqueio na `/api/v2/`.

---
<p align="center">
  <b>Research Module - Systems Security Engineering</b>
</p>
