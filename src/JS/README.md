
# Enterprise Security Lab (Java) ☕

Laboratório voltado para a análise de falhas em aplicações de larga escala, comuns em programas de Bug Bounty corporativos.

## 🛠 Ambiente de Trabalho
- **Runtime**: OpenJDK 17+ (Kali Linux default)
- **Tools**: `burpsuite` (para interceptar tráfego de apps Java), `nmap` (scripts NSE para Java RMI).

## 🎯 Foco de Pesquisa
- **Deserilização Insegura**: Como objetos maliciosos podem executar comandos no servidor.
- **Log4Shell & Dependency Analysis**: Análise de vulnerabilidades em bibliotecas externas.

## 🚀 Como Executar
```bash
javac VulnerableApp.java
java VulnerableApp
