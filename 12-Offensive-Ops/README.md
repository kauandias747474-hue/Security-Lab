# 🚩 Offensive Operations (Red Team) | Operações Ofensivas

> [!WARNING]
> **⚠️ AVISO LEGAL:** Todas as pesquisas e simulações aqui contidas são realizadas em ambientes controlados (Labs) e autorizados. O objetivo é fortalecer as defesas corporativas através da compreensão da mentalidade do adversário. O uso não autorizado destas técnicas é ilegal.

### 🇧🇷 Simulação de Adversários e Vetores de Ataque
O Red Teaming vai além do Pentest tradicional; ele foca em testar a capacidade de detecção e resposta de uma organização. Este módulo estuda a mentalidade do atacante para comprometer sistemas através de vetores técnicos e humanos. Pesquisamos como ataques de engenharia social, exfiltração de dados por protocolos não convencionais e técnicas de persistência podem ser utilizados para contornar perímetros de segurança modernos.

### 🇺🇸 Adversary Simulation and Attack Vectors
Red Teaming goes beyond traditional Pentesting; it focuses on testing an organization's detection and response capabilities. This module studies the attacker mindset to compromise systems through technical and human vectors. We research how social engineering, data exfiltration via unconventional protocols, and persistence techniques can be used to bypass modern security perimeters.

---

## 🔍 Áreas de Pesquisa | Research Areas

* **Ethical Phishing & Social Engineering:** Desenvolvimento de templates de login falsos e campanhas de conscientização utilizando o **SET (Social Engineering Toolkit)**.
* **Data Exfiltration:** Pesquisa de métodos para vazar dados sensíveis através de protocolos alternativos como **DNS e ICMP** para contornar inspeções de firewall (DLP Bypass).
* **Persistence & Lateral Movement:** Estudo de como atacantes mantêm acesso após o reboot e como se movem dentro de uma rede interna.
* **Payload Delivery:** Técnicas de entrega de executáveis e scripts que minimizam a detecção por soluções de antivírus tradicionais.

---



## 🧪 Laboratórios de Pesquisa | Research Labs

| Lab | Descrição (PT) | Description (EN) | Status |
| :--- | :--- | :--- | :--- |
| **[lab-ethical-phishing](./lab-ethical-phishing)** | Criação de páginas de captura de credenciais. | Creating credential harvesting pages. | ✅ |
| **[lab-dns-exfiltration](./lab-dns-exfiltration)** | Exfiltração de arquivos via túnel DNS. | File exfiltration via DNS tunneling. | 🧪 |
| **[lab-icmp-tunneling](./lab-icmp-tunneling)** | Encapsulamento de tráfego via pacotes ICMP. | Traffic encapsulation via ICMP packets. | 🛠️ |

---

## 🛠️ Toolstack
* **SET (Social Engineering Toolkit):** Framework para ataques de engenharia social.
* **Metasploit / Cobalt Strike (Concepts):** Orquestração de operações e beaconing.
* **DNSCat2 / Iodine:** Ferramentas para tunelamento DNS.
* **Wireshark:** Para análise e validação de padrões de exfiltração.

---
<p align="center">
  <b>Red Team Operations Module - Systems Security Engineering</b>
</p>
