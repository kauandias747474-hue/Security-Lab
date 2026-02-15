# 🎭 Lab: XSS Polyglots & Filter Bypass

### 🇧🇷 Diagnóstico: Pesquisa em Poliglotas XSS
Este repositório contém payloads "poliglotas" — strings híbridas projetadas para executar JavaScript em múltiplos contextos HTML simultaneamente (ex: dentro de uma tag, dentro de um atributo de evento ou em um bloco de script). O uso de poliglotas aumenta a eficiência da auditoria ao reduzir o número de requisições e contornar filtros de sanitização baseados em contexto.

### 🇺🇸 Diagnostic: XSS Polyglots Research
This repository contains "polyglot" payloads — hybrid strings designed to execute JavaScript in multiple HTML contexts simultaneously (e.g., inside a tag, within an event attribute, or in a script block). Using polyglots increases audit efficiency by reducing the number of requests and bypassing context-based sanitization filters.

---

## 🔬 Técnicas de Evasão | Evasion Techniques

* **Context Switching:** Payloads que fecham strings e tags dinamicamente.
* **Namespace Confusion:** Uso de tags `SVG` e `MathML` para executar código em parsers que ignoram tags HTML padrão.
* **Encoding Obfuscation:** Uso de entidades HTML e Unicode para esconder vetores de ataque.



## 🛠️ Conteúdo do Lab | Lab Content
* `payloads.txt`: Lista de poliglotas testados em WAFs modernos.
* `context-analysis.md`: Estudo sobre como cada caractere do payload quebra diferentes filtros.

---
