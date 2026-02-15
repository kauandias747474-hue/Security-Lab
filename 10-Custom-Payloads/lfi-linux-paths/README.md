# 📂 Lab: LFI to RCE Research | Pesquisa LFI para RCE

### 🇧🇷 Diagnóstico: Inclusão de Arquivos e Escala de Impacto
Diferente de um LFI básico, esta pesquisa foca em caminhos de arquivos que permitem a transição para **Remote Code Execution (RCE)**. Investigamos arquivos de log para técnicas de *Log Poisoning* e arquivos de sistema que expõem variáveis de ambiente e processos ativos.

### 🇺🇸 Diagnostic: File Inclusion and Impact Escalation
Unlike basic LFI, this research focuses on file paths that allow for a transition to **Remote Code Execution (RCE)**. We investigate log files for *Log Poisoning* techniques and system files that expose environment variables and active processes.

---

## 🔍 Foco da Pesquisa | Research Focus

* **Log Poisoning:** Caminhos como `/var/log/apache2/access.log` ou `/var/log/auth.log`.
* **Environment Extraction:** Acesso a `/proc/self/environ` para recuperar segredos de sessão.
* **Process Discovery:** Análise de `/proc/self/cmdline` para entender como o serviço backend foi iniciado.



## 🛠️ Conteúdo do Lab | Lab Content
* `lfi-linux-wordlist.txt`: Dicionário de caminhos críticos para sistemas baseados em Debian/CentOS.
* `rce-vectors.md`: Guia de como transformar a leitura de arquivo em execução de comando.

---
