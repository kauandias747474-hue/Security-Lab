# 🐳 Lab: Docker Breakout (Container Escape)

### 🇧🇷 Diagnóstico: Quebra de Isolamento
Este laboratório foca em cenários onde um container é executado com privilégios excessivos (modo --privileged) ou com o `docker.sock` montado. Demonstramos como um atacante que compromete o container pode assumir o controle total do host.

### 🇺🇸 Diagnostic: Isolation Breach
This lab focuses on scenarios where a container is run with excessive privileges (--privileged mode) or with the `docker.sock` mounted. We demonstrate how an attacker who compromises the container can take full control of the host.



## 🛡️ Mitigação
* Nunca rodar containers como root.
* Utilizar **Podman** ou configurar **User Namespaces** no Docker.
* Evitar montar sockets do Docker dentro de containers produtivos.
