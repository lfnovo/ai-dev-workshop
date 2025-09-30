
# Engineer Reason

Este é o comando para iniciar o planejamento de uma funcionalidade.

<arguments>
#$ARGUMENTS
</arguments>

## Análise

Leia os arquivos context.md e architecture.md na pasta .claude/sessions/<feature_slug> se ainda não tiver feito.

Sua tarefa agora é criar um plano de implementação detalhado (plan.md) para esta funcionalidade. O objetivo desta documentação é criar uma abordagem de implementação faseada que nos permita construir a funcionalidade incrementalmente, testando cada fase conforme avançamos. E também deve tornar possível retomar o trabalho caso nossa sessão seja interrompida.

O plan.md deve dividir a implementação em fases, cada fase com um pedaço do trabalho que pode ser realizado por um humano em 2 horas.

O template para o plan.md é:

<plan>
# [NOME DA FUNCIONALIDADE]

Se você está trabalhando nesta funcionalidade, certifique-se de atualizar este arquivo plan.md conforme progride.

## FASE 1 [Completada ✅]

Detalhes desta parte da funcionalidade

### Uma tarefa que foi feita [Completada ✅]

Detalhes sobre a tarefa

### Uma tarefa que foi feita [Completada ✅]

Detalhes sobre a tarefa

### Comentários:
- Algo que aconteceu e nos forçou a mudar de direção
- Algo que aprendemos durante o desenvolvimento
- Algo que discutimos e concordamos

## FASE 2 [Em Progresso ⏰]

### Uma tarefa que precisa ser feita [Em Progresso ⏰]

Detalhes sobre a tarefa

### Uma tarefa que precisa ser feita [Não Iniciada ⏳]

Detalhes sobre a tarefa

## FASE 3 [Não Iniciada ⏳]

### Uma tarefa que precisa ser feita [Não Iniciada ⏳]

Detalhes sobre a tarefa

### Uma tarefa que precisa ser feita [Não Iniciada ⏳]

Detalhes sobre a tarefa

</plan>


Dicas:
   - Analise detalhes específicos de implementação
   - Use WebSearch e ou context7 para melhores práticas ou documentação de bibliotecas (se necessário)

No caso desta pesquisa levantar uma nova decisão arquitetural ou contradição com as decisões anteriores, você iniciará uma discussão sobre isso com o humano, concordará com as mudanças e atualizará o documento architecture.md para aquela funcionalidade se necessário.

Este documento também deve anotar quais tarefas precisam ser feitas sequencialmente ou em paralelo.

Uma vez que o plan.md esteja finalizado, informe ao humano que você está pronto para prosseguir para o próximo passo.

