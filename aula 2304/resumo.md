# Aula 09: Introdução a Frameworks Back-end

## Comparação: Desenvolvimento Back-end (Puro vs. Framework)

| Aspecto | Desenvolvimento Sem Framework | Com Framework Back-end |
|----------|-------------------------------|-------------------------|
| **Rotas** | Manipulação manual de URLs complexas | Sistema de roteamento simples e organizado |
| **Segurança** | Vulnerável se não configurado do zero | Proteções nativas (CORS, Helmet, Auth) |
| **Banco de Dados** | Queries SQL manuais e repetitivas | Integração simplificada (ORMs/ODMs) |
| **Escalabilidade** | Difícil de manter em grandes sistemas | Arquitetura modular e padronizada |
| **Velocidade** | Desenvolvimento lento (configurações) | Desenvolvimento rápido (soluções prontas) |

---

## O que é um Framework Back-end?

Um framework back-end é um conjunto de ferramentas e convenções que padronizam a lógica do servidor. Ele não foca no que o utilizador vê, mas sim em como os dados são processados.

- **Foco Principal**: Lógica de servidor, APIs, segurança e ligação a bases de dados.
- **Padrão Comum**: Muitas vezes utiliza o padrão **MVC** (Model-View-Controller) para separar a lógica de negócio da interface.
- **Middleware**: Funções que correm entre o pedido do utilizador e a resposta final (ex: verificar se um utilizador está logado).



[Image of MVC architecture diagram]


---

## Introdução às APIs e REST

A comunicação entre o Front-end e o Back-end acontece através de APIs (Application Programming Interfaces).

- **REST (Representational State Transfer)**: Um estilo de arquitetura que utiliza métodos HTTP para operações:
    - `GET` → Procurar informação.
    - `POST` → Criar nova informação.
    - `PUT/PATCH` → Atualizar informação.
    - `DELETE` → Apagar informação.
- **JSON**: O formato padrão de troca de dados, leve e fácil de ler por máquinas e humanos.

---

## Express.js: O Framework para Node.js

O **Express.js** é o framework web mais popular para Node.js devido à sua simplicidade e performance.

### Características principais:
- **Minimalista**: Não impõe uma estrutura rígida, permitindo flexibilidade.
- **Programação Assíncrona**: Gere múltiplos pedidos em simultâneo sem bloquear o servidor.
- **Ecossistema**: Integra-se perfeitamente com bibliotecas de autenticação e bases de dados (como MongoDB ou MySQL).

---

## Estrutura de uma API com Express

Um projeto básico de Back-end geralmente contém:

- **`index.js` ou `server.js`**: Ponto de entrada onde o servidor é iniciado.
- **Routes**: Definição dos caminhos da API (ex: `/api/utilizadores`).
- **Controllers**: Onde reside a lógica que decide o que fazer com os dados.
- **Models**: Definição da estrutura dos dados que serão guardados.

---

## Ciclo de Vida: Do Pedido à Resposta

1. **Pedido (Request)**: O Front-end (React/Vue) pede dados via HTTP.
2. **Processamento**: O Express recebe o pedido, passa por middlewares (segurança/logs) e executa a lógica.
3. **Base de Dados**: Se necessário, o servidor procura ou guarda dados.
4. **Resposta (Response)**: O servidor envia os dados (geralmente em JSON) de volta com um código de status (ex: 200 OK ou 404 Not Found).