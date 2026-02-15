# 🛡️ Lab: SSL Pinning Bypass via Frida Injection

### 🇧🇷 Diagnóstico: Interceptação de Tráfego Protegido
O **SSL Pinning** é uma técnica onde o app valida o certificado do servidor contra um hash "hardcoded" no binário, impedindo ataques de Man-in-the-Middle (MitM) mesmo com certificados de confiança instalados. Este lab demonstra como contornar essa proteção em tempo de execução.

### 🇺🇸 Diagnostic: SSL Pinning Bypass via Frida Injection
**SSL Pinning** is a technique where the app validates the server's certificate against a hardcoded hash, preventing MitM attacks even with trusted certificates installed. This lab demonstrates how to bypass this protection at runtime.

---

## 🔬 O Ataque | The Attack
1. Tenta-se interceptar o tráfego com o **Burp Suite**, resultando em erro de conexão no app.
2. Utiliza-se o **Frida** para injectar um script JavaScript no processo do app.
3. O script faz o "hook" das funções de validação de certificado (ex: `TrustManager`) e força o retorno como "verdadeiro".

## 🛠️ Ferramentas & Scripts
* `bypass-pinning.js`: Script Frida para interceptação de funções nativas.
* `setup-proxy.sh`: Configuração de tabelas IP e redirecionamento de tráfego.

## 🛡️ Mitigação
* Implementação de verificações de integridade do binário para detetar se o processo foi "hookado".
* Uso de bibliotecas de pinning nativas e actualizadas (ex: Network Security Configuration no Android).

---
