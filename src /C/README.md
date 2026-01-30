
# Low-Level Security Lab (C) 🐧

Este diretório contém estudos de exploração de binários e manipulação de memória realizados no **Kali Linux**.

## 🛠 Ambiente de Testes
- **OS**: Kali Linux
- **Compiler**: `gcc`
- **Debuggers**: `gdb` (com plugin PEDA ou GEF)

## 🎯 Foco de Pesquisa
- **Buffer Overflow**: Estudo de estouro de pilha e sobrescrita de endereços de retorno.
- **Memory Management**: Identificação de Memory Leaks e Dangling Pointers.

## 🚀 Como Executar (Exemplo de Compilação)
Para testar vulnerabilidades desativando as proteções de memória do Kali:
```bash
gcc -fno-stack-protector -z execstack lab_vulnerable.c -o lab_vulnerable
