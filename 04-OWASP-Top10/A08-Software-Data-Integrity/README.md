# 🛡️ A08:2021 - Software and Data Integrity Failures | Falhas de Integridade de Software e Dados

### 🇧🇷 Diagnóstico de Integridade de Processos e Deserialização
Este laboratório foca na análise de falhas originadas pela confiança cega em fontes de dados, atualizações de software e pipelines de build sem a devida verificação de integridade. A pesquisa explora como a manipulação de objetos serializados e o comprometimento de cadeias de suprimentos (CI/CD) podem levar à Execução Remota de Código (RCE) e ao comprometimento total da infraestrutura de desenvolvimento.

### 🇺🇸 Software Integrity and Data Verification Diagnostic
This lab focuses on analyzing flaws stemming from blind trust in data sources, software updates, and build pipelines without proper integrity verification. The research explores how the manipulation of serialized objects and the compromise of supply chains (CI/CD) can lead to Remote Code Execution (RCE) and the total compromise of the development infrastructure.

---

## 🔬 Cenários de Pesquisa | Research Scenarios

Este módulo contém implementações práticas e metodologias de auditoria para os seguintes vetores:

1. **Insecure Deserialization (Deserialização Insegura):**
   - **🇧🇷 Cenário:** Manipulação de objetos serializados (JSON, XML ou binários) para forçar o interpretador a executar comandos maliciosos durante a reconstrução do objeto.
   - **🇺🇸 Focus:** Exploiting gadget chains to achieve RCE by tampering with serialized data streams.

2. **CI/CD Pipeline Poisoning (Envenenamento de Pipeline):**
   - **🇧🇷 Cenário:** Simulação de uma injeção de código malicioso em scripts de build ou automações de deploy que não possuem assinatura digital.
   - **🇺🇸 Focus:** Manipulating build artifacts and compromising the delivery flow of trusted software.

3. **Insecure Update Channels (Canais de Atualização Inseguros):**
   - **🇧🇷 Cenário:** Sequestro de mecanismos de atualização automática que baixam binários sem validar hashes ou assinaturas criptográficas.
   - **🇺🇸 Focus:** Researching Man-in-the-Middle (MITM) attacks on update mechanisms to deliver rogue patches.

4. **Missing Digital Signatures (Falta de Assinaturas Digitais):**
   - **🇧🇷 Cenário:** Distribuição de plugins ou módulos que são executados pelo sistema principal sem verificar a identidade do autor original.
   - **🇺🇸 Focus:** Bypassing integrity checks in modular architectures.

---



## 🛠️ Ferramentas de Auditoria (Audit Toolstack)

A metodologia de pesquisa utiliza as seguintes ferramentas para diagnóstico:
* **Ysoserial / GadgetProbe:** Geração de payloads para exploração de deserialização em diversas linguagens.
* **Burp Deserialization Scanner:** Identificação automatizada de pontos de entrada de dados serializados.
* **Hash Verification:** Uso de algoritmos de checksum (SHA-256) para garantir a integridade de artefatos de build.

---

## 🛡️ Arquitetura de Defesa Aplicada (Remediation)

A pesquisa conclui que a mitigação eficaz de falhas A08 exige:

* **Digital Signatures:** Uso obrigatório de assinaturas digitais e certificados para validar a origem de atualizações e plugins.
* **Safe Serialization:** Substituição de formatos de serialização perigosos por formatos de dados puros (como JSON estrito) ou uso de bibliotecas com listas de permissão (Allow-lists).
* **CI/CD Hardening:** Proteção de segredos no pipeline e revisão de código obrigatória para qualquer alteração em scripts de automação.
* **Integrity Checks:** Verificação sistemática de Hashes/Checksums antes da execução ou instalação de qualquer componente externo.

---

### 🚀 Como Executar | How to Run
1. Navegue até a subpasta do cenário (ex: `01-deserialization-lab`).
2. Inicie a aplicação: `node vulnerable-app.js`
3. Use o script Python para enviar um objeto serializado malicioso.
4. Veja a correção aplicada em `secure-deserialization.js` utilizando esquemas de validação de dados.

---
<p align="center">
  <b>Research Module - Systems Security Engineering</b>
</p>
