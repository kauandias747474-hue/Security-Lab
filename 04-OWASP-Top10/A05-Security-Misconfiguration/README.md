# ⚙️ A05:2021 - Security Misconfiguration | Laboratório de Pesquisa

### 🇧🇷 Diagnóstico de Endurecimento e Configuração de Sistemas
Este laboratório foca na análise de falhas resultantes de configurações de segurança incompletas, padrão ou inseguras em qualquer nível da stack. A pesquisa explora como o uso de credenciais de fábrica, serviços desnecessários ativos, mensagens de erro detalhadas e falta de cabeçalhos de proteção fornecem vetores de ataque críticos que expõem a infraestrutura e a lógica interna do sistema.

### 🇺🇸 Security Hardening & Misconfiguration Diagnostic
This lab focuses on analyzing flaws resulting from incomplete, default, or insecure security configurations across the stack. The research explores how default credentials, unnecessary active services, verbose error messages, and missing security headers provide critical attack vectors that expose infrastructure and internal system logic.

---

## 🔬 Cenários de Pesquisa | Research Scenarios

Este módulo contém implementações práticas dos seguintes vetores de falha e suas respectivas correções:

1. **Default Credentials & Admin Panels (Credenciais Padrão):**
   - **🇧🇷 Cenário:** Interfaces de gerenciamento ou bancos de dados acessíveis via combinações genéricas (ex: `admin:admin`).
   - **🇺🇸 Focus:** Directory enumeration and brute-force on exposed control panels.

2. **Directory Browsing & Path Disclosure (Listagem de Diretórios):**
   - **🇧🇷 Cenário:** Servidores web configurados para listar arquivos estruturais, expondo código-fonte ou assets sensíveis.
   - **🇺🇸 Focus:** Exploiting misconfigured web server settings to map application structure.

3. **Verbose Error Messages (Mensagens de Erro Detalhadas):**
   - **🇧🇷 Cenário:** Exposição de *Stack Traces*, versões de bibliotecas ou queries de banco de dados em respostas de erro (HTTP 500).
   - **🇺🇸 Focus:** Information gathering through application-level leakages to craft more precise attacks.

4. **Missing Security Headers (Cabeçalhos de Segurança Ausentes):**
   - **🇧🇷 Cenário:** Ausência de políticas como CSP, HSTS e X-Frame-Options, facilitando ataques de Clickjacking e Sniffing.
   - **🇺🇸 Focus:** Implementing security at the HTTP protocol level to harden the browser-server communication.

---



## 🛠️ Estrutura do Laboratório (Lab Structure)

Cada cenário dentro desta pasta está organizado da seguinte forma:

* **`misconfigured-app.js`**: Um serviço rodando com configurações propositadamente inseguras (ex: log de erro bruto).
* **`audit-report.md`**: Relatório técnico identificando as brechas de configuração e o risco associado.
* **`hardened-config.js`**: Implementação das correções de infraestrutura e aplicação de políticas de "Deny by Default".

---

## 🛡️ Arquitetura de Defesa Aplicada (Remediation)

A pesquisa conclui que a mitigação eficaz de falhas A05 exige:

* **Automated Hardening:** Uso de *Infrastructure as Code* (IaC) para garantir que ambientes de produção sejam idênticos e seguros.
* **Minimalist Surface:** Remoção de qualquer framework, driver ou funcionalidade que não seja essencial para o negócio.
* **Custom Error Handling:** Implementação de uma camada de tratamento que oculte detalhes técnicos do usuário final, registrando-os apenas em logs protegidos.
* **Credential Rotation:** Alteração obrigatória de toda e qualquer credencial padrão imediatamente após a instalação.

---

### 🚀 Como Executar | How to Run
1. Navegue até a subpasta do cenário (ex: `03-verbose-errors`).
2. Instale as dependências: `npm install`
3. Inicie o servidor: `node server.js`
4. Use o script de auditoria incluído ou ferramentas de inspeção para validar os vazamentos de configuração.

---
<p align="center">
  <b>Research Module - Systems Security Engineering</b>
</p>
