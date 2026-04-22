# Aula 07: Introdução a Frameworks Front-end

## Comparação: Desenvolvimento Vanilla vs. Framework

| Aspecto               | Vanilla JS (Puro)          | Framework Front-end                          |
| :-------------------- | :------------------------- | :------------------------------------------- |
| **Produtividade**     | Código manual e repetitivo | Acelerada por estruturas pré-definidas       |
| **Manutenção**        | Difícil escalabilidade     | Facilitada por componentes reutilizáveis     |
| **Fluxo de Trabalho** | Você decide a organização  | Segue padrões e convenções definidos         |
| **Interface (UI)**    | Manipulação manual do DOM  | Programação reativa (atualização automática) |
| **Uso Ideal**         | Scripts simples e pequenos | Aplicações web complexas e dinâmicas         |

---

## O Caos Antes dos Frameworks

Antes da popularização dos frameworks, o desenvolvimento front-end enfrentava desafios críticos:

- **🧱 Código Esparguete** → Sem uma estrutura clara, HTML, CSS e JS ficavam misturados e difíceis de ler.
- **🔄 Repetição Infindável** → Desenvolvedores precisavam "reinventar a roda" para funcionalidades comuns como rotas e gerenciamento de estado.
- **📉 Performance Ineficiente** → A manipulação direta do DOM real tornava as interfaces lentas em aplicações grandes.
- **🧩 Inconsistência** → Dificuldade em manter padrões visuais e lógicos em diferentes partes de um projeto grande.

---

## Benefícios do Uso de Frameworks

### 🍱 Componentização

Interfaces divididas em peças independentes e reutilizáveis que encapsulam sua própria lógica e estilo.

### ⚡ Virtual DOM (React)

Uso de uma cópia em memória do DOM para comparar mudanças e aplicar apenas o necessário, otimizando a velocidade.

### 🛠️ Ferramentas Integradas

Acesso nativo a sistemas de rotas (SPAs), integração com APIs e ferramentas de _build_.

### 🌍 Comunidade e Ecossistema

Documentação extensa e vasta biblioteca de plugins prontos para resolver problemas comuns.

---

# Ecossistema e Ferramentas

## O que é o React?

Tecnicamente uma **biblioteca** JavaScript criada pelo Facebook, mas utilizada como um framework para criar interfaces dinâmicas através de componentes.

## Node.js e NPM

- **Node.js**: Ambiente que permite executar JavaScript fora do navegador.
- **NPM**: Gerenciador de pacotes que automatiza a instalação de dependências (bibliotecas externas).

---

# Versionamento Semântico e Estrutura de Pastas

Ao criar um projeto React (ex: `npx create-react-app`), a estrutura facilita o versionamento:

- **`src/`**: Pasta com o código-fonte que **deve** ser versionada.
- **`node_modules/`**: Pasta de bibliotecas (deve ser ignorada pelo Git via `.gitignore`).
- **`package.json`**: Registra as versões exatas (SemVer) das dependências para garantir que a equipa use as mesmas versões.

---

# Deploy e Publicação

O ciclo final de desenvolvimento envolve tornar a aplicação acessível aos utilizadores:

## Fluxo de Deploy

1.  **Repositório Local**: Desenvolvimento e `commit` das alterações.
2.  **GitHub (Repositório Remoto)**: Sincronização do código para colaboração e backup.
3.  **Vercel (Produção)**: Plataforma que se conecta ao GitHub para realizar o **deploy automático**, gerando o link público da aplicação.

---

# Importância Geral para o Desenvolvedor

A adoção de frameworks aliada ao versionamento garante:

- **Organização Profissional**: Separação clara de responsabilidades no código.
- **Escalabilidade**: Facilidade para crescer o projeto sem perder o controlo.
- **Entrega Contínua**: Deploy simplificado e rápido para o utilizador final.
