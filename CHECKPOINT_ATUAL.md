# CHECKPOINT_ATUAL — VixDesk

- **Data da atualização:** 18/10/2026
- **Etapa do cronograma:** preparação inicial, antes da implementação
- **Último marco concluído:** documentos de contexto registrados no Git; repositório local limpo
- **Estado geral:** planejamento/documentação; aplicação ainda não implementada

## Estado confirmado por saídas do PowerShell

- Caminho do projeto: `C:\Users\aglib_i2fcqhe\Documents\Projetos\VixDesk`.
- `git --version` retornou `git version 2.51.0.windows.1`.
- `git branch --show-current` retornou `main`.
- `git rev-parse --show-toplevel` retornou `C:/Users/aglib_i2fcqhe/Documents/Projetos/VixDesk`.
- `git log -1 --oneline` retornou `e7d03ac (HEAD -> main) chore: add project context and initial setup`.
- `git status` retornou `On branch main` e `nothing to commit, working tree clean`.
- `.gitignore` existe na raiz; seu conteúdo foi conferido no terminal.
- `CHECKPOINT_ATUAL.md` existe na raiz.
- Estes quatro documentos estão em `docs/contexto/`: `CHECKPOINT_TEMPLATE.md`, `CONTEXTO_VIXDESK.md`, `DECISOES.md` e `PROTOCOLO_DE_CONTINUIDADE.md`.
- O commit atual existe. A mensagem de uma tentativa subsequente de `git commit` foi `nothing to commit, working tree clean`; isso significa que naquela tentativa não havia mudanças pendentes, não que o commit observado no log tenha falhado.

## Estrutura conhecida

```text
VixDesk/
├── .git/                         # repositório local
├── .gitignore                    # commit de documentação
├── CHECKPOINT_ATUAL.md           # checkpoint na raiz
└── docs/
    └── contexto/
        ├── CHECKPOINT_TEMPLATE.md
        ├── CONTEXTO_VIXDESK.md
        ├── DECISOES.md
        └── PROTOCOLO_DE_CONTINUIDADE.md
```

A estrutura acima é baseada nas saídas do terminal enviadas até agora; pode ser atualizada quando houver uma nova listagem completa.

## Git

- **Branch:** `main`.
- **Último commit observado:** `e7d03ac chore: add project context and initial setup`.
- **Estado observado:** árvore de trabalho limpa.
- **Repositório remoto:** não configurado/verificado.
- **Verificação adicional opcional:** `git show --stat --oneline HEAD` pode confirmar o resumo exato do commit.

## Confirmado, não implementado e não verificado

- **Confirmado:** pasta local, Git instalado, branch `main`, checkpoint na raiz, `.gitignore`, quatro documentos de contexto, commit no log e árvore de trabalho limpa.
- **Não implementado:** README principal, aplicação Spring Boot, Angular, schema de banco dedicado, autenticação, testes, Docker, CI/CD, integração n8n e implantação AWS.
- **Não verificado neste projeto:** versões/configuração de JDK, Node.js/npm, Angular CLI, Docker e PostgreSQL.
- **Nome VixDesk e domínio de sistema de chamados:** decisões de planejamento; verificar disponibilidade do nome antes de publicar.
- A AglibertoSTORE, os exercícios de programação e o estudo para o CRECI-ES pertencem a outras frentes e não devem ser misturados a este repositório.

## Próxima tarefa única

**Revisar o contexto e fechar os requisitos mínimos da primeira versão (MVP) antes de criar a aplicação.**

Critério de aceitação:
1. Definir os perfis e o fluxo principal de atendimento.
2. Listar os campos obrigatórios de um chamado e os estados permitidos.
3. Definir as primeiras operações da API e o que será deixado para depois.
4. Registrar as decisões em `DECISOES.md` e um documento `docs/REQUISITOS_MVP.md`.

Não criar código de aplicação antes de concluir essa definição. Não presumir que ferramentas foram instaladas ou testes executados.
