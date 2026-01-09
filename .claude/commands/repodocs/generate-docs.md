# Gerador de Documentação do Repositório

Você é um arquiteto de documentação técnica especializado em criar documentação abrangente e otimizada para IA de repositórios individuais. Sua missão é analisar a base de código do repositório e gerar uma estrutura completa de documentação na pasta `ai_docs/` que capture todos os aspectos importantes do projeto.

## Objetivo Principal

Gerar documentação completa do repositório na pasta `ai_docs/` que permita tanto desenvolvedores humanos quanto sistemas de IA compreender rapidamente:
- O propósito e papel do repositório
- A stack tecnológica e arquitetura utilizada
- Os padrões de design implementados
- As funcionalidades principais
- As regras de negócio aplicadas
- As APIs expostas (se aplicável)
- Os microserviços e suas regras (se aplicável)
- As integrações com outros repositórios e serviços
- Os "gotchas" e conhecimentos tácitos importantes

## Parâmetros de Entrada

**Argumentos Opcionais:**
Se você receber argumentos, eles podem conter informações adicionais sobre o repositório, como links para documentação externa, repositórios relacionados, ou contexto adicional. Use essas informações para enriquecer sua análise.

<arguments>
#$ARGUMENTS
</arguments>

## Framework de Análise

### Fase 1: Descoberta do Repositório

1. **Análise da Estrutura do Projeto**
   - Escanear estrutura de diretórios e identificar padrões arquiteturais
   - Analisar arquivos de dependência (package.json, requirements.txt, Cargo.toml, etc.)
   - Identificar sistemas de build, frameworks de teste e configurações
   - Detectar stack tecnológica, frameworks e bibliotecas principais
   - Identificar tipo de repositório (API, microserviço, biblioteca, frontend, etc.)

2. **Reconhecimento de Padrões Arquiteturais**
   - Identificar padrões de design (MVC, Clean Architecture, DDD, Event-Driven, etc.)
   - Analisar fluxo de dados e pontos de integração
   - Compreender arquitetura de deploy
   - Documentar abstrações e interfaces chave
   - Identificar camadas e responsabilidades

3. **Descoberta de Funcionalidades**
   - Mapear funcionalidades principais através da análise de código
   - Identificar endpoints, rotas, ou pontos de entrada
   - Compreender fluxos de trabalho principais
   - Documentar capacidades e casos de uso

4. **Análise de Regras de Negócio**
   - Identificar regras de negócio implementadas no código
   - Mapear validações, restrições e políticas
   - Documentar workflows e processos de negócio
   - Identificar cálculos, algoritmos e lógica complexa
   - Capturar invariantes e regras de domínio

5. **Mapeamento de Integrações**
   - Identificar comunicação com outros serviços/repositórios
   - Documentar APIs consumidas
   - Mapear dependências externas e internas
   - Identificar eventos publicados/consumidos
   - Documentar protocolos de comunicação (REST, GraphQL, gRPC, mensageria, etc.)

6. **Identificação de Gotchas**
   - Buscar por comentários TODO, FIXME, HACK, XXX, WORKAROUND no código
   - Identificar configurações não-óbvias ou contra-intuitivas
   - Detectar dependências de ordem de execução ou inicialização
   - Mapear comportamentos inesperados ou edge cases conhecidos
   - Identificar débitos técnicos documentados ou implícitos
   - Buscar por workarounds ou soluções temporárias que viraram permanentes

### Fase 2: Discussão com Usuário

Após construir uma boa compreensão do repositório, você fará ao usuário uma série de perguntas para esclarecer dúvidas ou informações faltantes. Planeje fazer entre 8-12 perguntas que cubram as áreas mais relevantes para este repositório específico.

**Áreas a explorar (adapte conforme o tipo de repositório):**

- **Propósito e Contexto**
  - Qual é o papel principal deste repositório no ecossistema da empresa?
  - Quem são os principais usuários/consumidores deste repositório?
  - Qual problema de negócio este repositório resolve?

- **Stack e Arquitetura**
  - Se não estiver claro: confirmar decisões tecnológicas principais
  - Por que estas escolhas tecnológicas foram feitas?
  - Existem planos de migração ou evolução da stack?

- **Funcionalidades**
  - Quais são as funcionalidades mais críticas?
  - Quais funcionalidades estão planejadas mas ainda não implementadas?
  - Existem funcionalidades deprecated ou em fase de remoção?

- **Regras de Negócio**
  - Quais são as regras de negócio mais complexas ou críticas?
  - Existem restrições regulatórias ou de compliance?
  - Quais validações são essenciais e por quê?

- **Para Repositórios de API**
  - Quais são os endpoints mais utilizados?
  - Qual é a estratégia de autenticação e autorização?
  - Existe documentação OpenAPI/Swagger disponível?
  - Quais são os limites de rate limiting?

- **Para Microserviços**
  - Qual é o domínio de responsabilidade deste serviço?
  - Como este serviço se comunica com outros serviços?
  - Quais eventos este serviço publica/consome?
  - Qual é a estratégia de resiliência e fallback?

- **Integrações**
  - Com quais outros repositórios/serviços este projeto se integra?
  - Quais são as dependências críticas?
  - Como é feita a comunicação entre serviços?

- **Padrões e Boas Práticas**
  - Quais padrões de design são utilizados e por quê?
  - Existem convenções específicas da equipe?
  - Quais são as práticas de teste adotadas?

- **Gotchas e Conhecimento Tácito**
  - Quais são as "armadilhas" que novos desenvolvedores costumam cair?
  - Existem comportamentos contra-intuitivos que precisam ser conhecidos?
  - Há dependências de ordem ou sequência que não são óbvias?
  - Quais workarounds existem e por que foram necessários?
  - Existem configurações que parecem erradas mas são intencionais?
  - O que você gostaria de ter sabido quando começou a trabalhar neste repositório?

Faça múltiplas rodadas de perguntas e respostas se sentir que ainda precisa obter mais informações.
Quando estiver pronto, dê ao usuário um resumo dos pontos mais importantes que detectou e peça aprovação para prosseguir para a fase 3.

### Fase 3: Geração de Documentação

Crie a pasta `ai_docs/` na raiz do repositório e gere os seguintes arquivos conforme aplicável ao tipo de repositório:

#### Criar Arquivo Índice (`ai_docs/index.md`)

```markdown
# Documentação do [Nome do Repositório]

## Visão Geral
[Breve descrição do propósito e papel do repositório]

## Documentação Disponível

### Arquitetura e Stack
- [Stack Tecnológica](stack.md) - Tecnologias, frameworks e ferramentas utilizadas
- [Padrões de Design](patterns.md) - Padrões arquiteturais e de código

### Funcionalidades e Regras
- [Funcionalidades](features.md) - Descrição das funcionalidades principais
- [Regras de Negócio](business-rules.md) - Regras de negócio implementadas
- [Gotchas](gotchas.md) - Armadilhas, workarounds e conhecimento tácito

### Integrações
- [Integrações](integrations.md) - Comunicação com outros serviços e repositórios

### APIs e Serviços
[Incluir apenas se aplicável]
- [Especificação de APIs](apis.md) - Endpoints, contratos e exemplos
- [Microserviços](services.md) - Regras e responsabilidades do microserviço

## Links Rápidos
- Repositório: [URL]
- Ambiente de Desenvolvimento: [Instruções]
- Deploy: [Processo]
```

#### Gerar Arquivos Individuais

**1. `ai_docs/stack.md`** (Obrigatório)
```markdown
# Stack Tecnológica

## Linguagens e Runtime
[Linguagens principais, versões, runtime]

## Frameworks Principais
[Frameworks utilizados e suas versões]

## Bibliotecas Chave
[Dependências principais e seus propósitos]

## Banco de Dados
[Bancos de dados utilizados, ORMs, estratégias de migração]

## Infraestrutura
[Deploy, containers, orquestração, cloud providers]

## Ferramentas de Desenvolvimento
[Linting, formatação, testes, CI/CD]

## Arquitetura Geral
[Visão geral da arquitetura: camadas, módulos principais, fluxo de dados]

## Decisões Arquiteturais Importantes
[Por que estas tecnologias foram escolhidas, trade-offs considerados]
```

**2. `ai_docs/patterns.md`** (Obrigatório)
```markdown
# Padrões de Design

## Padrões Arquiteturais
[Ex: MVC, Clean Architecture, Hexagonal, Event-Driven, etc.]

## Padrões de Código
[Ex: Factory, Repository, Strategy, Observer, etc.]

## Organização de Código
[Estrutura de pastas, módulos, responsabilidades]

## Convenções de Nomenclatura
[Padrões para nomes de arquivos, classes, funções, variáveis]

## Padrões de Teste
[Estratégias de teste unitário, integração, E2E]

## Padrões de Tratamento de Erros
[Como erros são tratados, logging, monitoramento]

## Boas Práticas Específicas
[Convenções da equipe, code reviews, etc.]
```

**3. `ai_docs/features.md`** (Obrigatório)
```markdown
# Funcionalidades

## Funcionalidades Principais

### [Nome da Funcionalidade 1]
**Descrição**: [O que faz]
**Casos de Uso**: [Quando é utilizada]
**Componentes Envolvidos**: [Módulos, classes, arquivos principais]
**Dependências**: [Outras funcionalidades ou serviços necessários]

### [Nome da Funcionalidade 2]
[...]

## Funcionalidades Secundárias
[Funcionalidades de suporte, utilitários, etc.]

## Funcionalidades em Desenvolvimento
[Roadmap, funcionalidades planejadas]

## Funcionalidades Deprecated
[Funcionalidades que estão sendo removidas ou substituídas]
```

**4. `ai_docs/business-rules.md`** (Obrigatório)
```markdown
# Regras de Negócio

## Regras Críticas

### [Nome da Regra 1]
**Descrição**: [Explicação da regra]
**Justificativa**: [Por que esta regra existe]
**Implementação**: [Onde no código está implementada]
**Validações**: [Quais validações são aplicadas]
**Exceções**: [Casos especiais ou exceções]

### [Nome da Regra 2]
[...]

## Validações e Restrições
[Validações de dados, constraints, invariantes]

## Políticas e Workflows
[Processos de negócio, fluxos de trabalho, estados]

## Cálculos e Algoritmos
[Lógica de cálculo, algoritmos complexos, fórmulas]

## Compliance e Regulamentações
[Requisitos legais, LGPD/GDPR, regulamentações específicas]

## Regras de Domínio
[Conceitos de domínio, invariantes, relacionamentos]
```

**5. `ai_docs/gotchas.md`** (Obrigatório)
```markdown
# Gotchas e Conhecimento Tácito

Este documento captura o conhecimento que desenvolvedores experientes acumulam ao longo do tempo - as "armadilhas" não documentadas, comportamentos contra-intuitivos e workarounds que são essenciais para trabalhar efetivamente neste repositório.

## Armadilhas Comuns

### [Nome da Armadilha 1]
**Sintoma**: [O que acontece quando você cai nessa armadilha]
**Causa**: [Por que isso acontece]
**Solução**: [Como evitar ou resolver]
**Contexto**: [Por que existe dessa forma]

### [Nome da Armadilha 2]
[...]

## Comportamentos Contra-Intuitivos

### [Comportamento 1]
**O que parece**: [O que você esperaria que acontecesse]
**O que realmente acontece**: [O comportamento real]
**Por quê**: [Justificativa ou histórico]
**Implicações**: [O que você precisa fazer diferente por causa disso]

### [Comportamento 2]
[...]

## Workarounds e Soluções Temporárias

### [Workaround 1]
**Problema Original**: [Qual problema isso contorna]
**Solução Aplicada**: [O que foi feito como workaround]
**Localização**: [Onde no código está implementado]
**Status**: [Temporário/Permanente, planos de remoção]
**Cuidados**: [O que não fazer para não quebrar o workaround]

### [Workaround 2]
[...]

## Dependências de Ordem e Sequência

### [Dependência 1]
**Contexto**: [Onde isso se aplica]
**Ordem Necessária**: [Qual sequência deve ser seguida]
**Consequência se Ignorado**: [O que acontece se a ordem não for respeitada]

### [Dependência 2]
[...]

## Configurações Não-Óbvias

### [Configuração 1]
**Configuração**: [Nome/caminho da configuração]
**Valor Atual**: [O que está configurado]
**Por que parece errado**: [Por que alguém poderia querer mudar]
**Por que está certo**: [Justificativa para manter assim]

### [Configuração 2]
[...]

## Débitos Técnicos Conhecidos

### [Débito 1]
**Descrição**: [O que é o débito técnico]
**Impacto**: [Como afeta o desenvolvimento]
**Origem**: [Como surgiu]
**Plano**: [Se existe plano para resolver]

### [Débito 2]
[...]

## Dicas de Desenvolvimento

### Ambiente Local
[Dicas para configurar e rodar o ambiente local]

### Debugging
[Dicas para debugar problemas comuns]

### Performance
[Armadilhas de performance a evitar]

### Testes
[Gotchas específicos de testes]

## O Que Eu Gostaria de Ter Sabido
[Lista de insights que desenvolvedores experientes compartilhariam com novatos]

- [Insight 1]
- [Insight 2]
- [...]
```

**6. `ai_docs/integrations.md`** (Obrigatório)
```markdown
# Integrações

## Repositórios e Serviços Relacionados

### [Nome do Serviço/Repositório 1]
**Tipo**: [API REST, gRPC, Mensageria, Biblioteca, etc.]
**Propósito**: [Por que esta integração existe]
**Protocolo**: [Como a comunicação é feita]
**Dados Trocados**: [Que informações são enviadas/recebidas]
**Dependência**: [Crítica, opcional, etc.]
**Tratamento de Falhas**: [Como falhas são tratadas]

### [Nome do Serviço/Repositório 2]
[...]

## Dependências Externas
[APIs de terceiros, serviços externos, cloud services]

## Eventos
[Se aplicável: eventos publicados e eventos consumidos]

## Contratos de Integração
[Schemas, interfaces, contratos de API]

## Resiliência
[Circuit breakers, retries, fallbacks, timeouts]
```

**7. `ai_docs/apis.md`** (Se aplicável - para repositórios que expõem APIs)
```markdown
# Especificação de APIs

## Visão Geral da API
[Descrição geral, propósito, versão]

## Autenticação e Autorização
[Métodos de autenticação, tokens, permissões]

## Endpoints

### [Método] /endpoint/path
**Descrição**: [O que este endpoint faz]
**Autenticação**: [Requerida/Opcional]
**Parâmetros**:
- Query: [...]
- Path: [...]
- Body: [...]

**Resposta de Sucesso**:
```json
{
  "exemplo": "de resposta"
}
```

**Códigos de Erro**:
- 400: [...]
- 401: [...]
- 500: [...]

**Exemplo de Uso**:
```bash
curl -X GET "https://api.example.com/endpoint"
```

[Repetir para cada endpoint importante]

## Rate Limiting
[Limites de requisições, quotas]

## Versionamento
[Estratégia de versionamento da API]

## Webhooks
[Se aplicável: webhooks disponíveis]

## OpenAPI/Swagger
[Link para documentação interativa se disponível]
```

**8. `ai_docs/services.md`** (Se aplicável - para microserviços)
```markdown
# Microserviço [Nome]

## Domínio de Responsabilidade
[Qual é a responsabilidade deste microserviço, bounded context]

## Regras do Serviço

### Regras de Negócio Específicas
[Regras implementadas especificamente neste serviço]

### Invariantes do Domínio
[Regras que devem sempre ser verdadeiras]

### Agregados e Entidades
[Principais conceitos de domínio gerenciados]

## Comunicação

### Endpoints Expostos
[APIs síncronas expostas]

### Eventos Publicados
[Eventos de domínio publicados]

### Eventos Consumidos
[Eventos que este serviço escuta]

### Comandos
[Comandos aceitos pelo serviço]

## Persistência
[Estratégia de armazenamento, banco de dados, schemas]

## Observabilidade
[Logs, métricas, traces, health checks]

## Resiliência e Escalabilidade
[Circuit breakers, auto-scaling, estratégias de recuperação]

## SLAs e SLOs
[Service Level Agreements e Objectives]
```

## Garantia de Qualidade

### Verificações de Qualidade do Conteúdo
- [ ] Todo conteúdo gerado é preciso em relação ao código real
- [ ] Exemplos estão funcionais e testados contra o projeto real
- [ ] Documentação arquitetural coincide com a implementação
- [ ] Todas as integrações críticas estão documentadas
- [ ] Regras de negócio capturam a lógica real implementada
- [ ] Gotchas e conhecimento tácito foram identificados e documentados
- [ ] Links internos entre arquivos funcionam corretamente

### Validação de Completude
- [ ] Todos os arquivos aplicáveis ao tipo de repositório foram criados
- [ ] Arquivos seguem a estrutura de template estabelecida
- [ ] Conteúdo é específico ao projeto, não genérico
- [ ] Funcionalidades principais estão documentadas
- [ ] Integrações com outros repositórios estão mapeadas
- [ ] Regras de negócio críticas estão explicadas

### Adaptação ao Tipo de Repositório
- [ ] Documentação reflete o tipo correto de repositório
- [ ] Arquivos opcionais (APIs, Services) foram incluídos quando relevantes
- [ ] Terminologia adequada ao domínio do repositório
- [ ] Nível de detalhe apropriado ao contexto

## Estratégia de Execução

1. **Análise Profunda Primeiro**: Gaste tempo significativo compreendendo o repositório antes de escrever
2. **Documentação Baseada em Evidências**: Toda informação deve ser baseada no código real
3. **Estrutura Modular**: Criar arquivos separados ligados através do índice
4. **Conteúdo Otimizado para IA**: Escrever tanto para consumo humano quanto da IA
5. **Detalhes Específicos**: Evitar informações genéricas; focar em especificidades reais
6. **Foco em Integrações**: Deixar muito claro como este repositório se relaciona com outros
7. **Regras de Negócio Explícitas**: Documentar não apenas o "como" mas também o "por quê"

## Critérios de Sucesso da Saída

A documentação gerada deve possibilitar:
- **Novos desenvolvedores** a compreender o repositório rapidamente e evitar armadilhas conhecidas
- **Sistemas de IA** a fornecer assistência precisa e contextual
- **Arquitetos** a compreender como este repositório se encaixa no sistema maior
- **Decisões técnicas** a serem tomadas com contexto completo
- **Planejamento de features** a identificar rapidamente onde implementar mudanças
- **Onboarding acelerado** ao expor conhecimento tácito que normalmente leva meses para adquirir

## Tratamento de Erros

Se certas informações não puderem ser determinadas a partir do código:
- Marcar claramente seções como "A SER COMPLETADO" com instruções específicas
- Fornecer templates para informações faltantes
- Referenciar de onde a informação deve vir
- Criar TODOs para trabalho de documentação de acompanhamento

## Notas Importantes

- Adapte a documentação ao **tipo específico de repositório**
- Não crie arquivos que não sejam relevantes (ex: apis.md para uma biblioteca)
- Foque em **clareza e precisão** sobre volume de informação
- Documente **relações e dependências** com outros repositórios
- Capture o **contexto de negócio**, não apenas a implementação técnica

Lembre-se: O objetivo é criar documentação que permita qualquer pessoa (humana ou IA) compreender rapidamente o propósito, funcionamento e relações deste repositório dentro do ecossistema maior da empresa.
