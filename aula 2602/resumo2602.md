# Versionamento e Deploy

## Comparação: Versionamento vs Backup

| Aspecto | Versionamento | Backup |
|----------|---------------|---------|
| Registro de alterações | Histórico completo de cada alteração | Cópia pontual do estado atual |
| Autoria | Registra quem, quando e por que mudou | Não há rastreio de autoria |
| Colaboração | Permite colaboração simultânea com merge | Arquivo único, sem controle de merge |
| Recuperação | Reversão granular (por commit específico) | Restauração total do arquivo |
| Rastreabilidade | Permite identificar exatamente o que mudou | Não permite análise detalhada |
| Conflitos | Detecta e auxilia na resolução de conflitos | Pode sobrescrever alterações |
| Uso ideal | Projetos colaborativos e desenvolvimento contínuo | Proteção contra perda de dados |

---

## O Caos Antes do Versionamento

Antes da adoção de sistemas de controle de versão, era comum enfrentar diversos problemas

- 📁 Arquivos Duplicados &rarr; Exemplo clássico:
    - 💾 versao_final_agora_sim2.zip &rarr;; Sem organização ou contexto claro das alterações.

- ⚠️ Conflito entre Desenvolvedores &rarr; Dois programadores editam o mesmo arquivo e um sobrescreve o trabalho do outro.

- 🔥 Código Perdido &rarr; Uma alteração incorreta pode apagar dias de trabalho sem possibilidade de recuperação.

- 🔎 Sem Histórico &rarr; Não é possível saber:
    - O que mudou  
    - Quem alterou  
    - Quando foi alterado  
    - Por que foi alterado  

---

## Benefícios do Versionamento

### 👥 Trabalho Simultâneo
Vários desenvolvedores podem atuar no mesmo projeto sem sobrescrever o trabalho uns dos outros.

### ⏱️ Menos Retrabalho
Conflitos são identificados cedo, evitando perda de horas de desenvolvimento.

### 📊 Auditoria e Rastreabilidade
Histórico completo contendo:
- Autor da modificação
- Data
- Alterações realizadas
- Justificativa (mensagem de commit)

### 🔄 Recuperação de Versões
Permite voltar para qualquer ponto do histórico com segurança, sem medo de perder progresso.

---

# Introdução ao Versionamento 

##  O que é Versionamento?

Versionamento é o processo de atribuir um identificador único a cada versão de um software ou documento.

Exemplos:
- Numérico: `v1.0`, `v1.1`, `v2.0`
- Baseado em data: `2023-10-01`

Ele registra:
- O que foi alterado
- Quem alterou
- Quando alterou
- Por que alterou

---

# Versionamento Semântico (SemVer)

O **Semantic Versioning (SemVer)** segue o padrão:

MAJOR > MINOR > PATCH

Exemplo: `2.1.3`

### Estrutura:

- **MAJOR (2.x.x)** → Mudanças incompatíveis com versões anteriores  
- **MINOR (x.1.x)** → Nova funcionalidade compatível  
- **PATCH (x.x.1)** → Correção de bug  

### Exemplos:

- `1.0.0` → Primeira versão estável  
- `1.1.0` → Nova funcionalidade  
- `1.1.1` → Correção de erro  
- `2.0.0` → Mudança que quebra compatibilidade  

### Vantagens:
- Clareza para desenvolvedores
- Melhor controle de dependências
- Previsibilidade na evolução do sistema

---

# Git – Sistema de Controle de Versão

## O que é Git?

Git é um sistema de controle de versão distribuído.

Ele:
- Registra mudanças no projeto
- Permite trabalhar offline
- Sincroniza com repositórios online (GitHub, GitLab)

---

## Estrutura do Git

- **Diretório de Trabalho** → Arquivos locais
- **Área de Staging** → Arquivos preparados para commit
- **Repositório Local** → Histórico de commits
- **Repositório Remoto** → Código hospedado online

---

## Commits

Commit é o registro de uma alteração no projeto.

Boas práticas:
- Commits pequenos e frequentes
- Mensagens claras e objetivas
- Explicar o que foi alterado e por quê

---

# Branches e Merge

## Branch

São ramificações do código que permitem trabalhar isoladamente.

Tipos comuns:
- `main` → Versão estável
- `develop` → Integração de funcionalidades
- `feature` → Nova funcionalidade
- `hotfix` → Correção urgente

## Merge

Processo de unir duas branches.

### Conflitos
Ocorrem quando duas alterações modificam a mesma parte do código.  
Devem ser resolvidos manualmente.

---

# Tags no Git

Tags são marcadores usados para identificar versões importantes.

Exemplo: `git tag 1.0.0`, `git push origin 1.0.0`


Tipos:
- Lightweight
- Annotated

São usadas para marcar releases estáveis.

---

# O que é Deploy?

Deploy é o processo de publicar o software em produção.

É a etapa que torna o sistema acessível aos usuários finais.

---

## Ambientes de Deploy

### 🖥️ Desenvolvimento
Ambiente local do programador.

### 🧪 Staging
Ambiente de testes finais antes da publicação.

### 🚀 Produção
Ambiente real acessado pelos usuários.

---

# Vercel para Deploy

Plataforma moderna de hospedagem que oferece:

- Integração com GitHub
- Deploy automático a cada push
- CDN global
- Serverless Functions
- Rollback rápido
- Alta performance e escalabilidade

Ideal para aplicações com React, Next.js, Vue e outras tecnologias modernas.

---

# Importância Geral do Versionamento

O controle de versão:

- Garante organização
- Permite colaboração eficiente
- Melhora qualidade do software
- Facilita auditoria
- Minimiza perda de trabalho
- Integra com ferramentas modernas (CI/CD)
