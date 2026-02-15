# 📦 A06:2021 - Vulnerable and Outdated Components | Componentes Vulneráveis e Desatualizados

### 🇧🇷 Diagnóstico de Integridade de Dependências e Supply Chain
Este laboratório foca na análise de riscos provenientes do uso de bibliotecas, frameworks e módulos de software obsoletos ou com vulnerabilidades conhecidas (CVEs). A pesquisa demonstra como a falta de uma política rigorosa de atualização e auditoria de terceiros pode comprometer a segurança de uma aplicação, mesmo que o código proprietário esteja seguro, explorando a cadeia de suprimentos (Supply Chain) e softwares sem patches.

### 🇺🇸 Dependency Integrity & Supply Chain Diagnostic
This lab focuses on analyzing risks arising from the use of libraries, frameworks, and other software modules that are old or have known vulnerabilities (CVEs). The research demonstrates how the lack of a strict update policy and third-party auditing can compromise an application's security, even if the proprietary code is secure, by exploiting the software supply chain and unpatched systems.

---

## 🔬 Cenários de Pesquisa | Research Scenarios

Este módulo contém implementações práticas e metodologias de auditoria para os seguintes vetores:

1. **Known CVE Exploitation (Exploração de CVEs):**
   - **🇧🇷 Cenário:** Simulação de um serviço utilizando uma versão vulnerável de uma biblioteca popular (ex: jQuery antigo ou bibliotecas de processamento de imagem).
   - **🇺🇸 Focus:** Identification and exploitation of publicly documented vulnerabilities using databases like NVD (National Vulnerability Database).

2. **Supply Chain Attacks (Ataques de Cadeia de Suprimentos):**
   - **🇧🇷 Cenário:** Análise de como pacotes maliciosos (Typosquatting) podem ser introduzidos via gerenciadores de pacotes (NPM/Yarn).
   - **🇺🇸 Focus:** Monitoring and detecting malicious code injection in third-party dependencies.

3. **Legacy Server Environment (Servidores sem Patch):**
   - **🇧🇷 Cenário:** Auditoria de versões de servidores web (Apache/Nginx) ou CMS (WordPress) com falhas conhecidas de execução remota de código (RCE).
   - **🇺🇸 Focus:** Exploiting unpatched infrastructure and version fingerprinting.

4. **Transitive Dependencies Risk (Dependências Transitivas):**
   - **🇧🇷 Cenário:** Investigação de vulnerabilidades em "dependências de dependências" que não aparecem diretamente no arquivo principal de manifesto.
   - **🇺🇸 Focus:** Deep scanning of dependency trees and the impact of indirect library vulnerabilities.

---



## 🛠️ Ferramentas de Auditoria (Audit Toolstack)

A metodologia de pesquisa utiliza as seguintes ferramentas para diagnóstico:
* **Snyk / NPM Audit:** Identificação automatizada de vulnerabilidades em manifestos.
* **Retire.js:** Scanner focado em bibliotecas JavaScript client-side obsoletas.
* **Searchsploit:** Busca local por exploits documentados para versões específicas de software.
* **OWASP Dependency-Check:** Análise de composição de software (SCA).

---

## 🛡️ Arquitetura de Defesa Aplicada (Remediation)

A pesquisa conclui que a mitigação eficaz de falhas A06 exige:

* **Continuous SCA (Software Composition Analysis):** Integração de ferramentas de análise de dependências diretamente no pipeline de CI/CD.
* **Virtual Patching:** Uso de Web Application Firewalls (WAF) para bloquear ataques conhecidos enquanto patches oficiais não são aplicados.
* **Automated Updates:** Implementação de ferramentas como Dependabot ou Renovate para manter bibliotecas atualizadas automaticamente.
* **Inventory Management:** Manutenção de um SBOM (Software Bill of Materials) detalhado para resposta rápida a novas CVEs.

---

### 🚀 Como Executar | How to Run
1. Navegue até a subpasta do cenário (ex: `01-cve-research`).
2. Execute o scanner de auditoria: `npm audit` ou use a ferramenta recomendada no lab.
3. Observe o relatório de vulnerabilidades e aplique a correção através do arquivo `mitigation.js` (ou `package-lock.json` atualizado).

---
<p align="center">
  <b>Research Module - Systems Security Engineering</b>
</p>
