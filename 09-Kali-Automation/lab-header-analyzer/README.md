# 📊 Script: header-analyzer.sh

### 🇧🇷 Descrição
Um utilitário de auditoria focado em conformidade Web. O script analisa milhares de domínios para verificar a presença e a configuração correta de cabeçalhos de segurança obrigatórios por normas de conformidade (como PCI-DSS e LGPD).

### 🇺🇸 Description
An audit utility focused on Web compliance. The script analyzes thousands of domains to verify the presence and correct configuration of security headers required by compliance standards (such as PCI-DSS and GDPR).

## 🛡️ Métricas de Auditoria
* Presença de **Content-Security-Policy (CSP)**.
* Configuração de **Strict-Transport-Security (HSTS)**.
* Identificação de cookies sem a flag `HttpOnly` ou `Secure`.
