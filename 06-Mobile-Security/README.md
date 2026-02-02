# 📱 Mobile App Security | Segurança de Apps Móveis

**EN:** Mobile apps often have fewer security layers than web versions. I focus on finding flaws in the binary and app communication.
**PT:** Apps móveis muitas vezes possuem menos camadas de segurança que versões Web. Foco em encontrar falhas no binário e na comunicação dos apps.

### 🔍 Research Areas | Áreas de Pesquisa:
* **Static Analysis:** Decompiling APKs with `JADX` to find hardcoded keys, API secrets, and staging URLs.
* **Dynamic Analysis:** Using `Frida` for **SSL Pinning Bypass** to intercept encrypted HTTPS traffic.
* **Insecure Storage:** Checking for sensitive data saved in `SharedPreferences` or local SQLite databases.

### 🛠️ Toolstack:
* Frida, Objection, JADX-GUI.
