# 🪣 Lab: S3 Bucket Misconfiguration & Data Leaks

### 🇧🇷 Diagnóstico: Armazenamento Mal Configurado
Um dos erros mais comuns na nuvem é deixar permissões de leitura pública em buckets sensíveis. Este laboratório demonstra como automatizar a descoberta destes buckets e como auditar se as políticas de acesso seguem o princípio do menor privilégio.

### 🇺🇸 Diagnostic: Misconfigured Storage
One of the most common cloud errors is leaving public read permissions on sensitive buckets. This lab demonstrates how to automate the discovery of these buckets and how to audit whether access policies follow the principle of least privilege.



## 🛠️ Conteúdo do Lab
* `bucket-finder.sh`: Script simples para testar acesso público em listas de nomes de buckets.
* `policy-audit.json`: Exemplo de uma política de bucket vulnerável vs. uma política endurecida.
