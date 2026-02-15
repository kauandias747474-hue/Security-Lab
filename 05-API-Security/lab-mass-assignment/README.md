# 💎 Lab: Mass Assignment & Privilege Escalation

### 🇧🇷 Diagnóstico: Atribuição em Massa
Esta falha ocorre quando a API aceita e processa inputs do usuário sem filtragem, permitindo que campos internos (como `is_admin` ou `account_balance`) sejam alterados através de um payload malicioso durante o cadastro ou atualização de perfil.

### 🇺🇸 Diagnostic: Mass Assignment
This flaw occurs when the API accepts and processes user inputs without filtering, allowing internal fields (such as `is_admin` or `account_balance`) to be modified via a malicious payload during registration or profile updates.

---

## 🔬 O Ataque | The Attack
O atacante intercepta a requisição de atualização de perfil e adiciona um campo não previsto:
```json
{
  "name": "Attacker",
  "email": "attacker@email.com",
  "role": "admin" 
}
