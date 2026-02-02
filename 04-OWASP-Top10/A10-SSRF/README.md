# A10:2021 - SSRF (Server-Side Request Forgery)

**PT-BR:** O SSRF ocorre quando uma aplicação web busca um recurso remoto sem validar a URL fornecida pelo usuário, permitindo acesso a sistemas internos.
**EN:** SSRF occurs when a web application fetches a remote resource without validating the user-supplied URL, allowing attackers to access internal systems.

### 🧪 Vetores de Ataque:
* **Exfiltração de Metadados de Cloud:** Acessar `169.254.169.254` para roubar tokens da AWS/Azure/GCP.
* **Scan de Rede Interna:** Mapear serviços internos (bancos de dados, painéis adm) a partir do servidor.
* **Bypass de Firewalls:** Fazer requisições para serviços rodando em `127.0.0.1`.

### 🛠️ Ferramentas:
* Burp Collaborator, Interactsh, Gopherus.
