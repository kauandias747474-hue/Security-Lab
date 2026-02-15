# 💣 Custom Payloads & Wordlists | Payloads e Wordlists Customizadas

> [!WARNING]
> **⚠️ USO ÉTICO:** O conteúdo deste módulo é destinado a testes de intrusão autorizados e ao fortalecimento de Web Application Firewalls (WAFs). O uso dessas strings para contornar proteções sem permissão é estritamente proibido.

### 🇧🇷 Pesquisa em Evasão e Vetores de Ataque
Ter suas próprias listas de teste é um diferencial crítico na segurança ofensiva. Este módulo organiza payloads e wordlists refinados através de pesquisas em cenários reais de auditoria. O foco não é apenas a quantidade, mas a qualidade técnica: strings desenhadas para identificar falhas de injeção e testar a resiliência de filtros modernos e WAFs contra técnicas de bypass.

### 🇺🇸 Evasion Research and Attack Vectors
Having your own test strings is a critical differentiator in offensive security. This module organizes payloads and wordlists refined through research in real-world audit scenarios. The focus is not just on quantity, but on technical quality: strings designed to identify injection flaws and test the resilience of modern filters and WAFs against bypass techniques.

---

## 🔍 Áreas de Pesquisa | Research Areas

* **XSS Bypass & Polyglots:** Payloads JavaScript projetados para contornar filtros de sanitização e detecção baseada em assinaturas de WAFs modernos.
* **LFI/RCE Discovery:** Listas de caminhos (paths) para arquivos críticos do sistema (Linux/Windows) e técnicas de *log poisoning* para teste de inclusão de arquivos.
* **SSTI (Server-Side Template Injection):** Strings de teste específicas para diversos motores de template (Jinja2, Mako, Thymeleaf, Smarty) focadas em execução de código remota.
* **Context-Specific Wordlists:** Listas de diretórios e parâmetros otimizadas para tecnologias específicas (ex: SAP, Kubernetes, Jenkins).

---



## 🧪 Repositórios de Payloads | Payload Repositories

| Categoria | Descrição (PT) | Description (EN) | Status |
| :--- | :--- | :--- | :--- |
| **[xss-polyglots](./xss-polyglots)** | Payloads que funcionam em múltiplos contextos HTML. | Payloads that work in multiple HTML contexts. | ✅ |
| **[lfi-linux-paths](./lfi-linux-paths)** | Caminhos críticos para auditoria de Local File Inclusion. | Critical paths for Local File Inclusion audits. | ✅ |
| **[ssti-detection](./ssti-detection)** | Polyglots para identificação de motores de template. | Polyglots for template engine identification. | 🧪 |

---

## 🛠️ Metodologia de Criação
1. **Análise de Filtro:** Estudo de como o WAF processa caracteres especiais (ex: `< > " ' ( )`).
2. **Encoding Research:** Uso de técnicas de Double URL Encoding, Hex e Unicode para ofuscação.
3. **Fuzzing de Contexto:** Teste de como o payload se comporta dentro de tags, atributos ou blocos de script.

---
<p align="center">
  <b>Research & Evasion Module - Systems Security Engineering</b>
</p>
