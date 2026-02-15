# 🌐 A10:2021 - SSRF (Server-Side Request Forgery) | Laboratório de Pesquisa

### 🇧🇷 Diagnóstico de Falsificação de Requisição do Lado do Servidor
Este laboratório foca na análise de falhas que permitem a um atacante induzir a aplicação a realizar requisições HTTP para destinos não planejados. A pesquisa demonstra como a falta de validação de URLs fornecidas pelo usuário pode ser explorada para acessar serviços internos protegidos por firewalls, realizar varreduras de rede local e exfiltrar credenciais sensíveis de metadados em ambientes de nuvem (AWS, Azure, GCP).

### 🇺🇸 Server-Side Request Forgery Diagnostic
This lab focuses on analyzing flaws that allow an attacker to induce the application to make HTTP requests to unintended destinations. The research demonstrates how the lack of validation for user-supplied URLs can be exploited to access internal services protected by firewalls, perform local network scans, and exfiltrate sensitive metadata credentials in cloud environments (AWS, Azure, GCP).

---

## 🔬 Cenários de Pesquisa | Research Scenarios

Este módulo contém implementações práticas e metodologias de auditoria para os seguintes vetores:

1. **Cloud Metadata Exfiltration (Exfiltração de Metadados):**
   - **🇧🇷 Cenário:** Requisições forjadas para o endereço IP link-local `169.254.169.254` para obter chaves de acesso e tokens de instâncias Cloud.
   - **🇺🇸 Focus:** Exploiting the cloud provider's metadata service to escalate privileges.

2. **Internal Port Scanning (Mapeamento de Rede):**
   - **🇧🇷 Cenário:** Uso da aplicação como proxy para identificar serviços rodando na rede interna (ex: Redis, MongoDB ou painéis de controle em `127.0.0.1`).
   - **🇺🇸 Focus:** Using the server as a pivot point to bypass network perimeter security.

3. **Bypassing Allow-lists (Bypass de Filtros):**
   - **🇧🇷 Cenário:** Técnicas para contornar filtros de domínio usando redirecionamentos, codificações hexadecimais ou serviços de DNS alternativos.
   - **🇺🇸 Focus:** Researching bypass techniques for poorly implemented URL validation logic.

4. **Protocol Smuggling (Exploração de Protocolos):**
   - **🇧🇷 Cenário:** Uso de esquemas de URL alternativos (como `file://`, `gopher://` ou `ftp://`) para ler arquivos locais ou interagir com outros protocolos.
   - **🇺🇸 Focus:** Abusing URI schemes to achieve local file disclosure (LFD) or deeper interaction with internal services.

---



## 🛠️ Ferramentas de Auditoria (Audit Toolstack)

A metodologia de pesquisa utiliza as seguintes ferramentas para diagnóstico:
* **Burp Collaborator / Interactsh:** Para detectar requisições "out-of-band" (OOB) originadas pelo servidor.
* **Gopherus:** Gerador de payloads para explorar SSRF via protocolos complexos (MySQL, Redis, etc).
* **DNSbin:** Testes de resolução de DNS para validar o impacto da vulnerabilidade.

---

## 🛡️ Arquitetura de Defesa Aplicada (Remediation)

A pesquisa conclui que a mitigação eficaz de falhas A10 exige:

* **Strict Allow-listing:** Implementação de uma lista rigorosa de domínios e protocolos permitidos, em vez de tentar bloquear endereços proibidos (Deny-list).
* **Input Validation:** Validação e sanitização de toda entrada de URL, impedindo o uso de IPs internos e esquemas de URI perigosos.
* **Network Segregation:** Isolamento da aplicação web em uma sub-rede que não tenha acesso direto a serviços críticos ou ao serviço de metadados da nuvem.
* **Response Handling:** Validação da resposta recebida para garantir que a aplicação não está servindo dados inesperados ao usuário final.

---

### 🚀 Como Executar | How to Run
1. Navegue até a subpasta do cenário (ex: `01-cloud-metadata`).
2. Inicie o servidor vulnerável: `node ssrf-app.js`
3. Execute o script de exploit para tentar acessar o "falso" serviço de metadados local.
4. Analise a proteção implementada em `secure-fetch.js` que utiliza filtros de rede e validação de IP.

---
<p align="center">
  <b>Research Module - Systems Security Engineering</b>
</p>
