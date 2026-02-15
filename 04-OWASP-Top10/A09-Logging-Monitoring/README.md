# 📉 A09:2021 - Security Logging and Monitoring Failures | Falhas de Registro e Monitoramento de Segurança

### 🇧🇷 Diagnóstico de Visibilidade e Resposta a Incidentes
Este laboratório foca na análise da incapacidade de sistemas em detectar, escalar e responder a atividades maliciosas em tempo real. A pesquisa explora como a ausência de logs detalhados, alertas mal configurados e a falta de monitoramento contínuo permitem que atacantes mantenham persistência em uma rede, realizem exfiltração de dados e apaguem seus rastros sem disparar alarmes.

### 🇺🇸 Security Visibility and Incident Response Diagnostic
This lab focuses on analyzing the inability of systems to detect, escalate, and respond to malicious activities in real-time. The research explores how the absence of detailed logs, misconfigured alerts, and lack of continuous monitoring allow attackers to maintain persistence, exfiltrate data, and cover their tracks without triggering alarms.

---

## 🔬 Cenários de Pesquisa | Research Scenarios

Este módulo contém implementações práticas e metodologias de auditoria para os seguintes vetores:

1. **Log Injection (Injeção de Log):**
   - **🇧🇷 Cenário:** Inserção de caracteres de quebra de linha (`\n`, `\r`) em campos de entrada para forjar entradas de log e confundir analistas ou ferramentas de SIEM.
   - **🇺🇸 Focus:** Neutralizing log forging attacks through proper sanitization of log entries.

2. **Insufficient Logging (Registro Insuficiente):**
   - **🇧🇷 Cenário:** Simulação de ataques críticos (ex: falhas de login, acesso a dados sensíveis) que não deixam rastros no sistema de arquivos ou banco de dados.
   - **🇺🇸 Focus:** Identifying which critical events must be logged to ensure a forensic trail.

3. **Inadequate Alerting (Alertas Inadequados):**
   - **🇧🇷 Cenário:** Execução de scripts de reconhecimento ou ataques de força bruta que não atingem o limite (threshold) de alerta da aplicação.
   - **🇺🇸 Focus:** Tuning alert thresholds to balance between "alert fatigue" and security visibility.

4. **Stealth Reconnaissance (Reconhecimento Furtivo):**
   - **🇧🇷 Cenário:** Testes de técnicas de evasão que exploram janelas de tempo onde o monitoramento é menos rigoroso ou inexistente.
   - **🇺🇸 Focus:** Measuring detection time and response effectiveness.

---



## 🛠️ Ferramentas de Auditoria (Audit Toolstack)

A metodologia de pesquisa utiliza as seguintes tecnologias para simulação:
* **ELK Stack (Elasticsearch, Logstash, Kibana):** Para centralização e visualização de logs de eventos.
* **Logman / Syslog:** Monitoramento de eventos a nível de sistema operacional.
* **Custom Watchers:** Scripts em Python para monitorar arquivos de log em tempo real e detectar padrões de ataque.

---

## 🛡️ Arquitetura de Defesa Aplicada (Remediation)

A pesquisa conclui que a mitigação eficaz de falhas A09 exige:

* **Centralized Logging:** Envio de logs para servidores seguros e isolados, impedindo que um atacante local possa apagá-los.
* **High-Value Logging:** Registro obrigatório de eventos de autenticação, controle de acesso e validação de entrada de dados.
* **Log Sanitization:** Tratamento de todas as entradas de log para evitar ataques de injeção e execução de scripts em painéis de monitoramento (XSS em SIEM).
* **Real-time Alerting:** Configuração de alertas para eventos de alto impacto com canais de notificação imediata.

---

### 🚀 Como Executar | How to Run
1. Navegue até a subpasta do cenário (ex: `01-log-injection`).
2. Inicie o serviço de registro: `node logging-app.js`
3. Execute o script de ataque para injetar entradas falsas: `python inject-logs.py`
4. Analise a diferença na integridade dos logs no arquivo `secure-logging.js`.

---
<p align="center">
  <b>Research Module - Systems Security Engineering</b>
</p>
