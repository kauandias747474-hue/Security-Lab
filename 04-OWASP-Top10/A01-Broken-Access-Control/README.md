# A01:2021 - Broken Access Control | Controle de Acesso Quebrado

**EN:** Access control enforces policy such that users cannot act outside of their intended permissions. Failures typically lead to unauthorized information disclosure, modification, or destruction of all data.
**PT:** O controle de acesso aplica políticas para que os usuários não possam agir fora das permissões pretendidas. Falhas levam à divulgação, modificação ou destruição não autorizada de dados.

### 🧪 Attack Vectors | Vetores de Ataque:
* **IDOR (Insecure Direct Object Reference):** Changing IDs in URLs to access other users' data.
* **Privilege Escalation:** Gaining administrative rights from a standard user account.
* **CORS Misconfiguration:** Exploiting overly permissive Cross-Origin Resource Sharing.
