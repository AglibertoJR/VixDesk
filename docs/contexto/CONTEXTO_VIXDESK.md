# VixDesk — Contexto oficial do projeto

**Versão do documento:** 1.1
**Data de atualização:** 18/10/2026
**Status:** planejamento; implementação ainda não iniciada neste projeto.

## 1. Objetivo

Criar uma aplicação full stack independente da AglibertoSTORE para estudar, em paralelo, tecnologias relevantes para vagas júnior e produzir um projeto de portfólio demonstrável. A meta é começar a se candidatar a vagas em até 50 dias, sem promessa de contratação nem de domínio completo de toda a stack.

## 2. Contexto de aprendizagem

- Considerar como base apenas o conteúdo até o exercício 54, conforme informado pelo usuário.
- Ensinar como para iniciante: explicar o conceito, demonstrar um exemplo pequeno, propor uma tarefa e revisar a solução do usuário.
- Não presumir que o usuário domina ferramentas apenas porque elas estão citadas no plano.
- O usuário estuda também pela Alura, pratica exercícios em outro chat, desenvolve a AglibertoSTORE em outro chat e prepara o concurso CRECI-ES em um chat separado. Este chat deve se concentrar exclusivamente no VixDesk e na preparação técnica associada.

## 3. Ideia do produto

**Nome provisório:** VixDesk. Confirmar disponibilidade do nome e do repositório antes de publicar.

Sistema de chamados de TI com três perfis previstos:
- Solicitante: abrir chamados, acompanhar status e responder.
- Técnico: atender chamados, registrar comentários e atualizar o andamento.
- Administrador: administrar usuários, permissões e indicadores.

Funcionalidades planejadas:
- Cadastro, listagem, consulta, edição e encerramento de chamados.
- Categoria, prioridade, status, responsável e datas relevantes.
- Comentários e histórico de alterações.
- Autenticação e autorização por perfil.
- Painel com indicadores e filtros.
- Documentação, testes, execução reproduzível e publicação, se viável.

A lista acima é planejamento, não funcionalidade existente.

## 4. Stack planejada

- Back-end: Java + Spring Boot, API REST.
- Banco de dados: PostgreSQL, SQL e Spring Data JPA.
- Front-end: Angular + TypeScript + Bootstrap.
- Segurança: Spring Security, BCrypt e JWT, após a base funcional.
- Qualidade: JUnit, Mockito e testes de integração; testes Angular conforme o tempo.
- API: Postman e OpenAPI/Swagger.
- Ambiente: Docker e Docker Compose.
- CI: GitHub Actions.
- Nuvem: AWS, com custos e limites verificados antes de criar recursos.
- Apoio: Git/GitHub e análise estática (por exemplo, SonarQube). n8n é opcional, somente após o fluxo principal funcionar.

Não incluir inicialmente microsserviços, Kubernetes, Kafka, pagamentos reais ou Terraform, salvo se o usuário alterar explicitamente o escopo.

## 5. Prazo de referência

Plano inicial de 50 dias: 19/10/2026 a 07/12/2026. O cronograma é uma meta flexível, não uma garantia. Priorizar entregas funcionais e compreensão sobre quantidade de tecnologias.

## 6. Arquitetura inicial prevista

Monólito modular, com front-end Angular separado do back-end Spring Boot e banco PostgreSQL. A estrutura desejada futuramente é:

```text
VixDesk/
├── backend/       # ainda não criado
├── frontend/      # ainda não criado
├── docs/
│   └── contexto/  # criado e confirmado
├── tests/         # ainda não criado
├── .gitignore     # criado e confirmado
├── CHECKPOINT_ATUAL.md  # criado na raiz e confirmado
└── README.md      # ainda não criado
```

## 7. Estado confirmado neste momento

Com base nas saídas do PowerShell enviadas em 18/10/2026:

- A pasta local existe em `C:\Users\aglib_i2fcqhe\Documents\Projetos\VixDesk`.
- O repositório Git local está inicializado e a branch atual é `main`.
- Git versão `2.51.0.windows.1` foi confirmado.
- O histórico apresenta o commit `e7d03ac` com a mensagem `chore: add project context and initial setup` (`git log -1 --oneline`).
- `git status` retornou `On branch main` e `nothing to commit, working tree clean`.
- `.gitignore` existe na raiz; seu conteúdo foi conferido no terminal.
- `CHECKPOINT_ATUAL.md` existe na raiz.
- Os arquivos `CHECKPOINT_TEMPLATE.md`, `CONTEXTO_VIXDESK.md`, `DECISOES.md` e `PROTOCOLO_DE_CONTINUIDADE.md` existem em `docs\contexto`.
- A árvore de trabalho foi confirmada limpa após o commit.
- O repositório remoto não foi configurado nem verificado.
- O projeto ainda está na fase de preparação; aplicação, back-end, front-end, banco de dados dedicado, testes e deploy não foram implementados/verificados.
- O conteúdo exato do commit ainda pode ser confirmado adicionalmente com `git show --stat --oneline HEAD`; essa verificação não foi incluída na saída compartilhada até agora.

## 8. Regras de fonte da verdade

1. Código, estrutura de pastas, saída de comandos e testes compartilhados pelo usuário nesta conversa são evidência do estado real.
2. Este documento resume decisões e objetivos; ele não comprova que funcionalidades foram implementadas.
3. Se este documento contradisser código recente compartilhado pelo usuário, apontar o conflito e atualizar o contexto com base na evidência mais recente.
4. Não afirmar que um comando foi executado, que um teste passou ou que um arquivo existe sem evidência.
5. Ao revisar código, pedir o arquivo completo e a mensagem de erro relevante quando o contexto fornecido não for suficiente; não inventar linhas ou classes existentes.
6. Distinguir claramente: **confirmado**, **proposto**, **pendente de verificação** e **não implementado**.
7. Evitar entregar a solução completa sem necessidade pedagógica. Orientar, deixar o usuário tentar e revisar, respeitando pedidos explícitos de dicas apenas.
8. Não avançar para a próxima etapa quando houver erro bloqueador no marco atual sem antes explicar e resolver ou registrar a limitação.
9. Toda mudança de escopo, stack ou decisão estrutural deve ser registrada em `DECISOES.md`.
10. Não colocar senhas, tokens, chaves privadas ou dados pessoais nos checkpoints. Usar nomes de variáveis como `DB_PASSWORD` e valores fictícios.

## 9. Critério de conclusão do projeto

O objetivo de 50 dias é ter, idealmente:
- aplicação funcionando e executável por instruções documentadas;
- código versionado e commits compreensíveis;
- fluxo principal testado;
- autenticação/autorização básicas revisadas;
- testes automatizados relevantes;
- documentação com arquitetura, setup, endpoints e exemplos;
- evidência de implantação ou um plano de deploy documentado se custos/limitações impedirem publicar;
- capacidade do usuário explicar as decisões principais em entrevista.

O cumprimento desses itens depende do progresso real; não declarar conclusão antecipadamente.
