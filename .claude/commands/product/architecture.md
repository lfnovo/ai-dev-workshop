
# Início da Engenharia

Este é o comando para disparar o início do design de arquitetura para uma funcionalidade.

## Análise

1. Passe pelos cards, pais e filhos se necessário, e construa um entendimento inicial do que precisa ser construído. Pense cuidadosamente sobre o que é solicitado, certifique-se de que entende exatamente:
    - Por que isso está sendo construído (contexto)
    - Qual é o resultado esperado para esta issue? (objetivo)
    - Como deve ser construído, apenas direcionalmente, não em detalhes (abordagem)
    - Se requer usar novas APIs/ferramentas, você as entende?
    - Como deve ser testado?
    - Quais são as dependências?
    - Quais são as restrições?

2. Depois de refletir sobre essas perguntas, elabore os 3-5 esclarecimentos mais importantes necessários para completar a tarefa.

3. Pergunte ao humano essas questões, ao mesmo tempo fornecendo seu entendimento e sugestões. PAUSE para aguardar as respostas do humano.

4. Depois de obter as respostas do humano, considere se precisa fazer mais perguntas. Se sim, faça mais perguntas ao humano. PAUSE para aguardar as respostas do humano.

5. Uma vez que tenha um bom entendimento do que está sendo construído, declare-o claramente de volta ao humano para revisão. Faça isso na forma de um artefato para que seja mais fácil de revisar.

6. Se o humano concordar com seu entendimento, você pode proceder para o próximo passo. Caso contrário, continue iterando juntos até obter aprovação explícita para prosseguir.

7. Se algo que vocês discutiram aqui afeta o que foi escrito nos requisitos, peça permissão ao humano para editar esses requisitos e fazer ajustes seja editando (mudanças estruturais) ou adicionando comentários (esclarecimentos). Se o requisito está em um card do Linear, edite o card do linear.

8. Não proceda para o próximo passo a menos que o humano tenha claramente dado o sinal verde nesta fase.

## Arquitetura

Dado seu entendimento do que será construído, você agora procederá ao desenvolvimento da arquitetura da funcionalidade. O documento de arquitetura deve mapear o que está sendo construído, os componentes, as dependências, os padrões, as tecnologias, as restrições, as suposições, os trade-offs, as alternativas, as consequências.

Aqui é onde você colocará seu chapéu de super pensamento e considerará o melhor caminho para construir a funcionalidade, ao mesmo tempo considerando os padrões e melhores práticas para este projeto.

1. Passe pelo código-fonte relevante, entenda sua estrutura e propósito e procure pelos arquivos importantes para esta implementação.

2. Revise os documentos de meta specs técnicas do projeto para garantir que esta funcionalidade se alinhe com nossa visão técnica

3. Construa uma proposta de arquitetura que se alinhe com os padrões e melhores práticas do projeto.

Dicas:
   - Use as ferramentas code-expert (se disponíveis) para encontrar arquivos específicos baseados nas respostas de descoberta
   - Mergulhe fundo em funcionalidades e padrões similares
   - Analise detalhes específicos de implementação
   - Use WebSearch ou context7 para melhores práticas ou documentação de biblioteca (se necessário)

Seu documento de arquitetura deve incluir:
    - Uma visão geral de alto nível do sistema (antes e depois da mudança)
    - Componentes afetados e seus relacionamentos, dependências
    - Padrões e melhores práticas que serão mantidos ou introduzidos
    - Dependências externas que serão usadas ou que precisam ser adicionadas ao projeto
    - Restrições e suposições
    - Trade-offs e alternativas
    - Consequências negativas (se houver) ao implementar este design
    - Lista dos principais arquivos a serem editados/criados

Se ajudar a construir um diagrama MERMAID, sinta-se livre para fazê-lo.

4. Se, em algum ponto, você tiver perguntas ou se encontrar algo que contradiz o que entendeu anteriormente, peça esclarecimento ao humano.

5. Uma vez que tenha um bom entendimento do que está sendo construído, mostre ao usuário na forma de um artefato e aguarde sua aprovação. Iterate juntos até estar pronto. PAUSE para aguardar a aprovação do humano.

6. Quando o humano concordar com seu entendimento, você pode proceder ao próximo passo, salvando os detalhes da arquitetura no card do linear como um comentário ao card original.

## Pesquisa

Se não tiver certeza de como uma biblioteca específica funciona, você pode usar Context7 e Perplexity para buscar informações sobre ela. Então, não tente adivinhar.

<feature_slug>
#$ARGUMENTS
</feature_slug>
