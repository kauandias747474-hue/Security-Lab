# 🕸️ Lab: GraphQL Denial of Service (DoS)

### 🇧🇷 Diagnóstico: Exaustão de Recursos via Queries Circulares
Diferente de APIs REST, onde os endpoints são estáticos, o GraphQL permite que o cliente defina a estrutura da resposta. Sem limites de profundidade (Depth Limits), um atacante pode criar uma query recursiva que explora relacionamentos (Ex: Usuário -> Post -> Usuário) para consumir 100% da CPU e RAM do servidor com uma única requisição.

### 🇺🇸 Diagnostic: Resource Exhaustion via Circular Queries
Unlike REST APIs with static endpoints, GraphQL allows the client to define the response structure. Without Depth Limits, an attacker can create a recursive query exploiting relationships (e.g., User -> Post -> User) to consume 100% of server CPU and RAM with a single request.

---

## 🔬 O Ataque | The Attack
O atacante identifica um relacionamento circular e envia uma query com aninhamento excessivo:
```graphql
query {
  user(id: "1") {
    posts {
      author {
        posts {
          author {
            # Repetição profunda que gera uma carga massiva no Banco de Dados
          }
        }
      }
    }
  }
}
