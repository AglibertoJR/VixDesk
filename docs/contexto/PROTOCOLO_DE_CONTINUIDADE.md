# Protocolo de continuidade e prevenção de alucinações — VixDesk

## A. Regras para cada sessão

No início de uma sessão de implementação:
1. Consultar `CONTEXTO_VIXDESK.md` e o último `CHECKPOINT_ATUAL.md` disponível.
2. Identificar o último marco concluído e a próxima tarefa pequena.
3. Se uma decisão depender do estado do código, pedir/verificar os arquivos ou comandos atuais em vez de inferir.
4. Registrar pressupostos explicitamente antes de dar comandos que possam alterar ou apagar dados.

Ao propor código:
- Indicar o caminho do arquivo.
- Dizer se é arquivo novo ou alteração de arquivo existente.
- Explicar o propósito e os conceitos novos.
- Evitar substituir arquivos inteiros quando um ajuste pequeno bastar.
- Não misturar várias tecnologias novas na mesma tarefa sem necessidade.
- Não pedir credenciais reais. Usar variáveis de ambiente e placeholders.

Ao validar:
- Informar o comando exato a executar.
- Separar resultado esperado de resultado efetivamente observado.
- Só marcar testes/build como aprovados depois que o usuário compartilhar a saída ou houver execução real disponível.
- Em erro, resolver primeiro a causa demonstrada; não mudar várias coisas por tentativa aleatória.

## B. Checkpoints obrigatórios

Criar/atualizar `CHECKPOINT_ATUAL.md`:
- ao concluir cada etapa de 5 dias do plano;
- após uma decisão arquitetural relevante;
- antes de migrar para um chat novo;
- quando o usuário disser que a conversa está ficando longa.

O checkpoint deve incluir:
1. Data e última atualização.
2. Etapa atual e último marco concluído.
3. Estrutura real das pastas (confirmada por saída de comando).
4. Arquivos importantes e o que cada um faz.
5. Funcionalidades concluídas, em andamento e pendentes.
6. Comandos executados e resultados comprovados.
7. Último commit/hash e estado do Git, se fornecidos.
8. Erros conhecidos e tentativas já feitas.
9. Próxima tarefa única, com critério de aceitação.
10. Decisões e dúvidas ainda abertas.

Não preencher lacunas com suposições. Escrever “não verificado” quando faltar evidência.

## C. Como retomar em um chat novo

Enviar estes arquivos:
- `CONTEXTO_VIXDESK.md`
- `PROTOCOLO_DE_CONTINUIDADE.md`
- `DECISOES.md`
- `CHECKPOINT_ATUAL.md` mais recente

Anexar também os arquivos do código ou a saída relevante de comandos. Instrução de retomada sugerida:

> Leia os documentos anexados como contexto do VixDesk. Diferencie fatos confirmados de itens planejados. Não suponha estado do código sem evidência. Resuma em até 10 linhas o estado atual e retome apenas a próxima tarefa do checkpoint. Não trabalhe na AglibertoSTORE nem no chat de exercícios/CRECI-ES.

## D. Verificação rápida do estado Git

Executar na pasta real do projeto:

```powershell
git status --short
git log -5 --oneline
git branch --show-current
```

Para mapear arquivos sem listar dependências:

```powershell
Get-ChildItem -Recurse -File |
  Where-Object { $_.FullName -notmatch '\\(\.git|target|node_modules|dist)\\' } |
  Select-Object -ExpandProperty FullName
```

Compartilhar as saídas relevantes; revisar antes de publicar qualquer segredo.

## E. Comandos destrutivos

Antes de recomendar exclusão, limpeza de banco, reset de Git, sobrescrita de arquivo ou remoção de recursos AWS:
1. explicar exatamente o que será apagado/alterado;
2. verificar se há backup ou commit recuperável;
3. preferir uma opção não destrutiva;
4. pedir confirmação explícita quando houver risco de perda de trabalho.

## F. Controle de escopo

Prioridade: fluxo de chamados funcional → qualidade e segurança → Docker/CI → AWS e acabamento. Tecnologias opcionais não devem atrasar o fluxo principal. Nenhuma ferramenta será marcada como dominada só por ter sido instalada ou mencionada.
