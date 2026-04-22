# Aula 08: Atividade com Projetos Front-end

## Comparação: NPM vs. Downloads Manuais

| Aspecto           | Gerenciador de Pacotes (NPM)          | Download Manual                       |
| ----------------- | ------------------------------------- | ------------------------------------- |
| **Instalação**    | Automatizada via linha de comando     | Download de ficheiros .zip ou .js     |
| **Dependências**  | Gere automaticamente sub-dependências | Necessário baixar cada ficheiro extra |
| **Atualização**   | Comando simples (`npm update`)        | Substituição manual de ficheiros      |
| **Espaço**        | Organizado na pasta `node_modules`    | Ficheiros espalhados pelo projeto     |
| **Versionamento** | Registado no `package.json`           | Sem registo formal de versão          |

---

## O Ecossistema Node.js

Para trabalhar com frameworks modernos, é indispensável o uso do **Node.js**:

- **Node.js** → Ambiente que permite executar JavaScript fora do navegador (no servidor ou computador local).
- **NPM (Node Package Manager)** → Gerenciador que acompanha o Node.js e automatiza a instalação de bibliotecas.
- **Teste de Instalação** → Verificação via terminal: `node --version` e `npm --version`.

---

## Criação de Projetos (Scaffolding)

A aula foca no uso de ferramentas de linha de comando (CLI) para "gerar" a estrutura inicial dos principais frameworks:

### ⚛️ React

Utiliza o comando `npx create-react-app nome-do-projeto`.

- Cria uma estrutura pronta com servidor de desenvolvimento integrado.

### 🅰️ Angular

Utiliza o Angular CLI: `npm install -g @angular/cli` e depois `ng new nome-do-projeto`.

- Estrutura mais rígida e completa (opinativa).

### 🟢 Vue.js

Utiliza o comando `npm init vue@latest`.

- Foco em simplicidade e performance.

---

## Estrutura Padrão de um Projeto Framework

Ao criar qualquer um destes projetos, a estrutura segue uma lógica comum:

- **`node_modules/`** → Contém todas as bibliotecas instaladas (MUITO pesada, nunca deve ser enviada para o Git).
- **`package.json`** → O "bilhete de identidade" do projeto. Contém o nome, versão e a lista de dependências.
- **`src/`** → Onde o código-fonte da aplicação reside (Componentes, CSS, Imagens).
- **`public/`** → Ficheiros estáticos que não passam pelo processo de compilação.

---

## Fluxo de Trabalho: Importação e Execução

Para trabalhar num projeto que já existe (ex: descarregado do GitHub):

1. **📦 Instalação**: O comando `npm install` lê o ficheiro `package.json` e descarrega todas as bibliotecas necessárias para a pasta `node_modules`.
2. **🚀 Execução**: O comando `npm start` (React) ou `npm run dev` (Vue/Vite) inicia o servidor local.
3. **🛠️ Build**: O comando `npm run build` prepara os ficheiros para o **Deploy** (produção).

---

## Atividade Prática: Deploy na Vercel

O objetivo final é a publicação do projeto criado:

- **Passo 1**: Criar o projeto localmente.
- **Passo 2**: Criar um repositório no **GitHub** e fazer o `push` do código (exceto a pasta `node_modules`).
- **Passo 3**: Ligar a conta do GitHub à **Vercel**.
- **Passo 4**: Configurar o deploy automático para que cada alteração no código atualize o site em tempo real.

---

## Importância da Automação

O uso de frameworks e CLIs (Command Line Interfaces) garante que o ambiente de desenvolvimento seja **replicável**. Qualquer programador da equipa pode baixar o código, rodar um comando e ter exatamente a mesma aplicação a funcionar.
