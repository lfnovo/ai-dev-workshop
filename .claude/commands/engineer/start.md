
# Engineer Start

Este é o comando para iniciar o desenvolvimento de uma funcionalidade.

## Configuração
- Se não estivermos em uma feature branch, peça permissão para criar uma
- Se estivermos em uma feature branch que corresponde ao nome da funcionalidade, estamos prontos.
- Certifique-se de que existe uma pasta .claude/sessions/<feature_slug>
- Peça ao usuário o input para esta sessão (você receberá um ou mais cards do Linear para trabalhar)

## Análise

Analise os cards, pais e filhos se necessário, e construa um entendimento inicial do que precisa ser desenvolvido. Pense cuidadosamente sobre o que é solicitado, certifique-se de entender exatamente:
    - Por que isso está sendo construído (contexto)
    - Qual é o resultado esperado para esta issue? (objetivo)
    - Como deve ser construído, apenas direcionalmente, não em detalhes (abordagem)
    - Se requer o uso de novas APIs/ferramentas, você as entende?
    - Como deve ser testado?
    - Quais são as dependências?
    - Quais são as restrições?

Após refletir sobre essas questões, formule as 3-5 clarificações mais importantes necessárias para completar a tarefa. Pergunte essas questões ao humano, enquanto também fornece seu entendimento e sugestões.

Depois de obter as respostas do humano, considere se precisa fazer mais perguntas. Se sim, faça mais perguntas ao humano.

Uma vez que tenha um bom entendimento do que está sendo construído, salve-o no arquivo .claude/sessions/<feature_slug>/context.md e peça ao humano para revisar.

Se o humano concordar com seu entendimento, você pode prosseguir para o próximo passo. Caso contrário, continue iterando juntos até obter aprovação explícita para seguir em frente.

Se algo que você discutiu aqui afeta o que foi escrito nos requisitos, peça permissão ao humano para editar esses requisitos e fazer ajustes seja editando (mudanças estruturais) ou adicionando comentários (clarificações).

Se o requisito estiver em um card do Linear, edite o card do Linear.
Se o requisito for de um arquivo de texto, edite o arquivo de texto.

IMPORTANT: Neste momento, PARE e espere a aprovação expressa do usuario antes de continuar. 

## Arquitetura

Dado seu entendimento do que será construído, você agora procederá ao desenvolvimento da arquitetura da funcionalidade. O documento de arquitetura deve mapear o que está sendo construído, os componentes, as dependências, os padrões, as tecnologias, as restrições, as suposições, os trade-offs, as alternativas, as consequências.

É aqui que você colocará seu chapéu de pensamento ultra e considerará o melhor caminho para construir a funcionalidade, considerando também os padrões e melhores práticas deste projeto.

Nesta seção, espera-se que você analise o código fonte relevante, entenda sua estrutura e propósito, e então construa uma arquitetura que se alinha com os padrões e melhores práticas do projeto.

Dicas:
   - Use mcp__RepoPrompt__search (se disponível) para encontrar arquivos específicos baseados nas respostas de descoberta
   - Use mcp__RepoPrompt__set_selection e read_selected_files (se disponível) para ler código relevante em batch
   - Mergulhe fundo em funcionalidades e padrões similares
   - Analise detalhes específicos de implementação
   - Use WebSearch e ou context7 para melhores práticas ou documentação de bibliotecas (se necessário)

Seu documento de arquitetura deve incluir:
    - Uma visão geral de alto nível do sistema (antes e depois da mudança)
    - Componentes afetados e suas relações, dependências
    - Padrões e melhores práticas que serão mantidos ou introduzidos
    - Dependências externas que serão usadas ou que precisam ser adicionadas ao projeto
    - Restrições e suposições
    - Trade-offs e alternativas
    - Consequências negativas (se houver) da implementação deste design
    - Lista dos principais arquivos a serem editados/criados

Se ajudar a construir um diagrama MERMAID, sinta-se livre para fazê-lo.

Se, a qualquer momento, você tiver dúvidas ou encontrar algo que contradiga o que entendeu anteriormente, peça esclarecimentos ao humano.

Uma vez que tenha um bom entendimento do que está sendo construído, salve-o no arquivo .claude/sessions/<feature_slug>/architecture.md e peça ao humano para revisar.

Se o humano concordar com seu entendimento, você pode prosseguir para o próximo passo. Caso contrário, continue iterando juntos até obter aprovação explícita para seguir em frente.

Uma vez que o architecture.md esteja finalizado, informe ao humano que você está pronto para prosseguir para o próximo passo.

## Pesquisa

Se você não tem certeza de como uma biblioteca específica funciona, você pode usar Context7 e Perplexity para buscar informações sobre ela. Então, não tente adivinhar.

<feature_slug>
#$ARGUMENTS
</feature_slug>
