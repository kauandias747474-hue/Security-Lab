# 🔍 Lab: Static Analysis & Hardcoded Secrets

### 🇧🇷 Diagnóstico: Exposição de Segredos em Análise Estática
A análise estática envolve descompilar o binário para ler o código-fonte original. Este lab demonstra como chaves de API, credenciais de bases de dados de staging e segredos criptográficos são frequentemente esquecidos dentro do código.

### 🇺🇸 Diagnostic: Static Analysis & Hardcoded Secrets
Static analysis involves decompiling the binary to read the original source code. This lab demonstrates how API keys, staging database credentials, and cryptographic secrets are often forgotten within the code.

---

## 🔬 O Ataque | The Attack
1. O ficheiro APK é descompilado utilizando o **JADX-GUI**.
2. Realiza-se uma busca por strings sensíveis (ex: `API_KEY`, `AWS_SECRET`, `firebase`).
3. Descoberta de endpoints de teste que permitem acesso a funcionalidades não publicadas.

## 🛠️ Ferramentas
* **JADX / Bytecode Viewer**: Para descompilação de DEX para Java.
* **Strings utility**: Para extração rápida de texto de binários compilados.

## 🛡️ Mitigação
* Ofuscação de código (ProGuard/R8) para dificultar a leitura.
* Armazenamento de segredos em servidores externos ou utilização de **Secret Management Services** em tempo de execução.

---
