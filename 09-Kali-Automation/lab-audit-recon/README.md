# 🚀 Script: audit-recon.sh

### 🇧🇷 Descrição Técnico-Científica
Este script executa uma varredura sistemática de ativos para fins de inventário e auditoria. Ele não busca "bugs" de forma aleatória, mas sim cataloga a superfície de ataque, identificando domínios, endereços IP e as tecnologias associadas, gerando um relatório estruturado em formato JSON/CSV.

### 🇺🇸 Technical-Scientific Description
This script performs a systematic asset scan for inventory and auditing purposes. It does not look for "bugs" randomly but catalogs the attack surface, identifying domains, IP addresses, and associated technologies, generating a structured report in JSON/CSV format.



## ⚙️ Fluxo de Trabalho | Workflow
1. **Discovery**: Enumeração de ativos via fontes de DNS passivas e ativas.
2. **Resolution**: Resolução de IP e validação de conectividade.
3. **Fingerprinting**: Extração de `Server` headers e tecnologias (via Wappalyzer/httpx).
