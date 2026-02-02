# A07:2021 - Falhas de Identificação e Autenticação

**PT-BR:** A confirmação da identidade do usuário, autenticação e gestão de sessão são críticas para proteger contra ataques de sequestro de conta.
**EN:** Confirmation of the user's identity, authentication, and session management is critical to protect against authentication-related attacks.

### 🧪 Vetores de Ataque:
* **Credential Stuffing:** Usar listas de senhas vazadas para tentar acesso em massa.
* **Força Bruta (Brute Force):** Atacar endpoints de login que não possuem limite de tentativas (rate-limiting).
* **Bypass de MFA:** Burlar a lógica de autenticação de dois fatores.
* **Fixação de Sessão:** Forçar um usuário a usar um ID de sessão conhecido pelo atacante.

### 🛠️ Ferramentas:
* Burp Suite Intruder, Hydra, FFuf (fuzzing de credenciais).
