# 📡 Lab: DNS Exfiltration (DLP Bypass)

### 🇧🇷 Diagnóstico: Exfiltração via Protocolos de Infraestrutura
Muitos firewalls permitem tráfego DNS de saída sem restrições. Este lab pesquisa como codificar dados sensíveis (como chaves de API ou documentos) dentro de subdomínios de consultas DNS para "vazar" informações sem disparar alertas de rede.

### 🇺🇸 Diagnostic: Exfiltration via Infrastructure Protocols
Many firewalls allow unrestricted outbound DNS traffic. This lab researches how to encode sensitive data (like API keys or documents) within DNS query subdomains to "leak" information without triggering network alerts.



## 🛡️ Mitigação
* Monitoramento de anomalias em logs de DNS (consultas muito longas ou frequentes).
* Implementação de inspeção profunda de pacotes (DPI).
