# ☁️ Cloud & Container Security | Segurança em Nuvem e Containers

### 🇧🇷 Diagnóstico: Vulnerabilidades em Ambientes Cloud Native
A modernização da infraestrutura trouxe novos desafios. Este módulo foca na pesquisa de vulnerabilidades em ambientes de nuvem e orquestração. Investigamos desde falhas básicas de configuração em serviços de armazenamento (S3 Buckets) até técnicas complexas de escape de containers e abuso de permissões em políticas de IAM. O objetivo é garantir que a agilidade da nuvem não comprometa a integridade dos dados e o isolamento dos processos.

### 🇺🇸 Diagnostic: Cloud Native Environment Vulnerabilities
Modern infrastructure has brought new challenges. This module focuses on researching vulnerabilities in cloud and orchestration environments. We investigate everything from basic misconfigurations in storage services (S3 Buckets) to complex container escape techniques and IAM policy abuse. The goal is to ensure that cloud agility does not compromise data integrity and process isolation.

---

## 🔍 Áreas de Pesquisa | Research Areas

* **S3 Buckets & Cloud Storage:** Identificação de permissões mal configuradas (Public Read/Write) que levam a vazamentos de dados massivos.
* **Docker/K8s Breakout:** Técnicas de "fuga de container" para ganhar acesso ao host e abuso de APIs de orquestração (Kubernetes) para movimentação lateral.
* **IAM Roles & Privilege Escalation:** Pesquisa sobre escalada de privilégios através de permissões mal configuradas no AWS IAM ou Azure AD.
* **Secret Management:** Auditoria de segredos (chaves de API, senhas) expostos em variáveis de ambiente, Dockerfiles ou metadados da nuvem.

---



## 🧪 Laboratórios de Nuvem | Cloud Labs

| Lab | Descrição (PT) | Description (EN) | Status |
| :--- | :--- | :--- | :--- |
| **[lab-s3-misconfig](./lab-s3-misconfig)** | Identificação de buckets expostos e coleta de dados. | Finding exposed buckets and data harvesting. | ✅ |
| **[lab-docker-escape](./lab-docker-escape)** | Escala de privilégio via Docker Socket (/var/run/docker.sock). | Privilege escalation via Docker Socket. | 🧪 |
| **[lab-iam-escalation](./lab-iam-escalation)** | Abuso de permissões `AssumeRole` para acesso admin. | Abusing `AssumeRole` permissions for admin access. | 🛠️ |

---

## 🛠️ Toolstack de Pesquisa
* **AWS CLI / Azure CLI:** Para interação direta com APIs de nuvem.
* **TruffleHog / GitLeaks:** Ferramentas para encontrar segredos expostos.
* **Kube-hunter / Peirates:** Ferramentas de auditoria e ataque para Kubernetes.
* **CloudSplaining:** Analisador de políticas de IAM para identificar riscos.

---
<p align="center">
  <b>Cloud Security Research Module - Systems Security Engineering</b>
</p>
