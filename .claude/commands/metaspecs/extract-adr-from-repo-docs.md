# Extrator de ADRs (Architecture Decision Records) do Repositório

Você é um arquiteto de software especializado em documentar decisões arquiteturais. Sua missão é analisar a documentação existente de um repositório e extrair as **decisões arquiteturais fundamentais** que moldaram o projeto, documentando-as no formato ADR (Architecture Decision Record).

## Objetivo Principal

Identificar e documentar as **decisões arquiteturais significativas** do repositório em formato ADR, criando uma coleção de documentos que capture:
- Decisões técnicas e arquiteturais importantes
- Contexto que levou a cada decisão
- Alternativas consideradas
- Consequências e trade-offs
- Status atual de cada decisão

Além dos ADRs, criar documentação complementar sobre:
- Arquitetura geral do sistema e comunicação entre componentes
- Visão geral das decisões (índice anotado)

## Parâmetros de Entrada

**Argumentos Opcionais:**
Se você receber argumentos, eles podem conter informações adicionais sobre aspectos específicos a serem analisados ou contexto adicional sobre o repositório.

<arguments>
#$ARGUMENTS
</arguments>

## Framework de Análise

### Fase 1: Análise da Documentação e Código

**Fontes Primárias a Analisar:**

1. **Pasta `docs/`** (fonte principal)
   - Todos os arquivos markdown da documentação
   - Focar em seções que explicam decisões e justificativas
   - Identificar padrões arquiteturais adotados

2. **Arquivos de Configuração**
   - `.editorconfig`, `.prettierrc`, `eslint.config.js`, etc.
   - `pyproject.toml`, `setup.cfg`, `Cargo.toml`, `package.json`, etc.
   - `Dockerfile`, `docker-compose.yml`
   - Arquivos de CI/CD (`.github/workflows/`, `.gitlab-ci.yml`, etc.)
   - Configurações de infraestrutura (Terraform, K8s, etc.)

3. **Arquivos de Documentação Raiz**
   - `README.md`
   - `ARCHITECTURE.md`
   - `CONTRIBUTING.md`
   - Qualquer `ADR` ou `meta/adr/` existente

4. **Análise do Código**
   - Estrutura de pastas e organização
   - Padrões arquiteturais implementados
   - Abstrações e interfaces principais
   - Estratégias de comunicação entre componentes
   - Dependências e integrações

**Categorias de Decisões Arquiteturais a Identificar:**

#### 1. Decisões de Stack Tecnológica
- Escolha de linguagem de programação
- Frameworks principais (web, teste, etc.)
- Bancos de dados e sistemas de persistência
- Bibliotecas e dependências críticas

#### 2. Decisões Arquiteturais
- Padrão arquitetural (MVC, Clean Architecture, Hexagonal, Event-Driven, etc.)
- Separação de camadas e responsabilidades
- Estratégia de modularização
- Arquitetura de deploy (monolito, microserviços, serverless)

#### 3. Decisões de Comunicação e Integração
- Protocolos de comunicação (REST, gRPC, GraphQL, mensageria)
- Estratégias de sincronização vs. assincronismo
- APIs internas vs. externas
- Contratos e versionamento

#### 4. Decisões de Dados
- Modelagem de dados
- Estratégias de migração
- Caching e performance
- Consistência vs. disponibilidade (CAP theorem)

#### 5. Decisões de Qualidade e Operações
- Estratégia de testes
- Observabilidade (logs, métricas, traces)
- Estratégias de deploy e rollback
- Tratamento de erros e resiliência

#### 6. Decisões de Segurança
- Autenticação e autorização
- Gerenciamento de segredos
- Estratégias de validação
- Compliance e auditoria

#### 7. Decisões de Desenvolvimento
- Convenções de código e formatação
- Processo de code review
- Estratégias de branching e versionamento
- Ferramentas de desenvolvimento

### Fase 2: Validação com Usuário

Após a análise, apresente ao usuário as decisões arquiteturais identificadas. Para cada decisão:

**Formato de Apresentação:**
```markdown
## Decisão Identificada: [Título]

**Contexto Inferido**: [O que parece ter motivado esta decisão]
**Decisão**: [O que foi decidido]
**Evidências**: [Onde observei esta decisão - arquivos, padrões, configurações]
**Alternativas Possíveis**: [Outras opções que provavelmente foram consideradas]
**Consequências Observadas**: [Impactos visíveis no código/arquitetura]
**Incertezas**: [O que preciso confirmar]
```

**Perguntas para Validação:**

1. **Confirmação de Decisões**
   - "Estas decisões foram conscientes e intencionais?"
   - "Existem decisões importantes que não identifiquei?"
   - "Alguma destas 'decisões' foi na verdade acidental/herdada?"

2. **Contexto e Motivação**
   - "Qual era o problema/contexto que levou à decisão X?"
   - "Que alternativas foram realmente consideradas?"
   - "Houve algum evento/requisito específico que forçou esta decisão?"

3. **Consequências e Trade-offs**
   - "Quais foram os principais trade-offs desta decisão?"
   - "Houve consequências inesperadas (positivas ou negativas)?"
   - "Se fosse fazer hoje, faria diferente?"

4. **Status das Decisões**
   - "Esta decisão ainda está ativa e sendo seguida?"
   - "Alguma decisão foi superseded (substituída) por outra?"
   - "Existem decisões que estão deprecated e sendo migradas?"

5. **Detalhes Técnicos**
   - Para cada decisão, confirmar detalhes técnicos específicos
   - Validar minha compreensão das alternativas consideradas
   - Esclarecer métricas de sucesso ou critérios de avaliação usados

**Iteração**: Continue o diálogo até ter informações suficientes para escrever ADRs completos e precisos.

### Fase 3: Geração da Documentação ADR

Crie a estrutura de documentação ADR no repositório:

#### Estrutura de Pastas

```
meta/
├── adr/
│   ├── README.md                    # Índice e explicação dos ADRs
│   ├── 0001-use-python-as-language.md
│   ├── 0002-adopt-clean-architecture.md
│   ├── 0003-use-postgresql-database.md
│   ├── 0004-implement-event-driven-pattern.md
│   └── ...
└── architecture/
    ├── system-overview.md           # Visão geral da arquitetura
    └── communication-patterns.md    # Como componentes se comunicam
```

#### 1. Arquivo Índice: `meta/adr/README.md`

```markdown
# Architecture Decision Records (ADRs)

Este diretório contém os registros de decisões arquiteturais (ADRs) do projeto [Nome do Repositório].

## O que é um ADR?

Um ADR (Architecture Decision Record) é um documento que captura uma decisão arquitetural importante, incluindo o contexto que a motivou, as alternativas consideradas e as consequências da escolha.

## Índice de Decisões

### Decisões Ativas

| ADR | Título | Status | Data |
|-----|--------|--------|------|
| [0001](0001-use-python-as-language.md) | Use Python as Primary Language | Ativa | YYYY-MM-DD |
| [0002](0002-adopt-clean-architecture.md) | Adopt Clean Architecture | Ativa | YYYY-MM-DD |
| [0003](0003-use-postgresql-database.md) | Use PostgreSQL as Database | Ativa | YYYY-MM-DD |
| ... | ... | ... | ... |

### Decisões Superseded (Substituídas)

| ADR | Título | Substituída por | Data |
|-----|--------|-----------------|------|
| [00XX](00XX-old-decision.md) | Old Decision | ADR 00YY | YYYY-MM-DD |

### Decisões Deprecated (Descontinuadas)

| ADR | Título | Razão | Data |
|-----|--------|-------|------|
| [00ZZ](00ZZ-deprecated-decision.md) | Deprecated Decision | [Razão] | YYYY-MM-DD |

## Categorias de Decisões

### Stack Tecnológica
- ADR 0001: Use Python as Primary Language
- ADR 00XX: ...

### Arquitetura
- ADR 0002: Adopt Clean Architecture
- ADR 00XX: ...

### Dados e Persistência
- ADR 0003: Use PostgreSQL as Database
- ADR 00XX: ...

### Comunicação e Integração
- ADR 00XX: ...

### Segurança
- ADR 00XX: ...

### Operações e Deploy
- ADR 00XX: ...

## Como Propor um Novo ADR

[Instruções para a equipe criar novos ADRs]

1. Copie o template de ADR
2. Numere sequencialmente (próximo número disponível)
3. Preencha todas as seções
4. Submeta para review

## Template ADR

Ver [template.md](template.md) para o formato padrão.

## Documentação Relacionada

- [Visão Geral da Arquitetura](../architecture/system-overview.md)
- [Padrões de Comunicação](../architecture/communication-patterns.md)
```

#### 2. Template ADR: `meta/adr/template.md`

```markdown
# [Número]. [Título Curto e Descritivo]

Data: YYYY-MM-DD

## Status

[Proposta | Aceita | Superseded por ADR-00XX | Deprecated | Rejeitada]

## Contexto

[Descreva o contexto e o problema que motivou esta decisão.
O que estava acontecendo? Que forças estavam em jogo?
Que requisitos ou restrições existiam?]

## Decisão

[Descreva a decisão tomada de forma clara e direta.
"Vamos..." ou "Decidimos..."]

## Alternativas Consideradas

### Alternativa 1: [Nome]
**Descrição**: [Como funcionaria]
**Prós**:
- [Vantagem 1]
- [Vantagem 2]

**Contras**:
- [Desvantagem 1]
- [Desvantagem 2]

**Razão para rejeição**: [Por que não escolhemos esta]

### Alternativa 2: [Nome]
[...]

## Consequências

### Positivas
- [Consequência positiva 1]
- [Consequência positiva 2]

### Negativas
- [Consequência negativa 1]
- [Consequência negativa 2]

### Neutras
- [Mudanças necessárias]
- [Impactos em outros sistemas]

## Trade-offs

[Descreva explicitamente os trade-offs feitos. O que sacrificamos em favor de quê?]

## Notas de Implementação

[Detalhes técnicos relevantes para implementação]
[Links para código, PRs, ou documentação técnica]

## Validação

[Como saberemos se esta decisão foi bem-sucedida?]
[Métricas ou critérios de avaliação]

## Revisão

[Data da última revisão]: [Resultado - decisão ainda válida? Precisa ajustes?]
```

#### 3. ADRs Individuais

Para cada decisão identificada, crie um arquivo seguindo o template acima. **Exemplo:**

**Arquivo: `meta/adr/0001-use-python-as-language.md`**

```markdown
# 1. Use Python as Primary Language

Data: 2024-01-15

## Status

Ativa

## Contexto

O projeto necessitava de uma linguagem que permitisse desenvolvimento rápido,
tivesse um ecossistema rico de bibliotecas para machine learning e data science,
e fosse familiar para a equipe existente. A escolha da linguagem fundamental
impacta todas as outras decisões técnicas do projeto.

Requisitos considerados:
- Produtividade de desenvolvimento
- Disponibilidade de bibliotecas especializadas (ML, data processing)
- Facilidade de contratação e onboarding
- Performance adequada para casos de uso esperados
- Suporte a type hints para maior segurança

## Decisão

Vamos usar Python 3.11+ como linguagem principal do projeto, com uso obrigatório
de type hints e ferramentas de análise estática (mypy, ruff).

## Alternativas Consideradas

### Alternativa 1: Go
**Descrição**: Usar Go como linguagem principal
**Prós**:
- Performance superior
- Concorrência nativa eficiente
- Binary compilado facilita deploy
- Type safety mais forte

**Contras**:
- Ecossistema de ML/data science menos maduro
- Curva de aprendizado para equipe atual
- Desenvolvimento potencialmente mais lento
- Menos flexibilidade para prototipagem rápida

**Razão para rejeição**: A velocidade de desenvolvimento e ecossistema de
bibliotecias especializadas do Python superam as vantagens de performance do Go
para nosso caso de uso atual.

### Alternativa 2: TypeScript/Node.js
**Descrição**: Usar TypeScript no backend
**Prós**:
- Compartilhamento de código com frontend
- Performance adequada
- Type safety built-in
- Ecosistema npm rico

**Contras**:
- Bibliotecas de ML/data science menos maduras
- Equipe tem mais experiência com Python
- Ferramentas científicas/matemáticas limitadas

**Razão para rejeição**: Ecossistema de data science/ML do Python é decisivo
para nossos casos de uso principais.

## Consequências

### Positivas
- Desenvolvimento rápido com código conciso
- Acesso a bibliotecas especializadas (pandas, scikit-learn, etc.)
- Fácil integração com Jupyter notebooks para análise
- Equipe já tem expertise significativa
- Comunidade ativa e recursos abundantes

### Negativas
- Performance inferior a linguagens compiladas
- GIL (Global Interpreter Lock) limita concorrência multi-thread
- Type safety requer disciplina com type hints
- Gestão de dependências pode ser complexa
- Packaging e distribuição mais trabalhosos

### Neutras
- Necessidade de usar ferramentas adicionais (mypy, ruff) para qualidade
- Deploy requer runtime Python no ambiente
- Consideração de performance requirements em features críticas

## Trade-offs

Priorizamos **velocidade de desenvolvimento e ecossistema especializado** sobre
**performance e type safety forte**. Aceitamos a necessidade de ferramentas
adicionais para compensar a tipagem dinâmica.

## Notas de Implementação

- Usar `uv` para gerenciamento de dependências (mais rápido que pip/poetry)
- Configurar mypy em modo strict
- Usar ruff para linting e formatação
- Python 3.11+ para aproveitar melhorias de performance
- Considerar Cython ou extensões C para partes críticas de performance

Ver: `pyproject.toml` para configurações completas

## Validação

Decisão será considerada bem-sucedida se:
- Velocity de desenvolvimento permanece alta (>= 2 story points/dev/sprint)
- Performance atende SLAs definidos (< 100ms p95 para APIs críticas)
- Onboarding de novos devs <= 2 semanas para produtividade
- Qualidade de código mantida (< 5 bugs/1000 LOC)

## Revisão

**2024-06-15**: Revisado. Decisão permanece válida. Performance tem sido adequada.
Type hints aumentaram significativamente qualidade do código.
```

#### 4. Visão Geral da Arquitetura: `meta/architecture/system-overview.md`

```markdown
# Visão Geral da Arquitetura

> Última atualização: [Data]
>
> Este documento fornece uma visão de alto nível da arquitetura do sistema,
> mostrando como os componentes principais se organizam e interagem.

## Diagrama de Arquitetura de Alto Nível

```
[Incluir diagrama - pode ser ASCII art, Mermaid, ou link para imagem]
```

## Componentes Principais

### [Componente 1]

**Responsabilidade**: [O que este componente faz]
**Tecnologias**: [Stack usada]
**Decisões Relacionadas**: [Links para ADRs relevantes]
**Dependências**: [Outros componentes dos quais depende]
**Consumidores**: [Quem usa este componente]

### [Componente 2]
[...]

## Camadas Arquiteturais

[Se aplicável - descrever as camadas e suas responsabilidades]

### Camada 1: [Nome]
**Responsabilidade**: [...]
**Componentes**: [...]
**Regras**: [Restrições e convenções]

## Fluxo de Dados

[Descrever como dados fluem através do sistema]

1. [Passo 1]
2. [Passo 2]
3. [...]

## Decisões Arquiteturais Chave

Esta arquitetura foi moldada pelas seguintes decisões principais:

- [ADR 0002: Adopt Clean Architecture](../adr/0002-adopt-clean-architecture.md)
- [ADR 00XX: ...](../adr/00XX-....md)
- [...]

## Princípios Arquiteturais

[Princípios fundamentais que guiam a arquitetura]

1. **[Princípio 1]**: [Descrição e justificativa]
2. **[Princípio 2]**: [Descrição e justificativa]
3. [...]

## Estratégias Transversais

### Tratamento de Erros
[Como erros são tratados através do sistema]

### Logging e Observabilidade
[Estratégia de logs, métricas, traces]

### Segurança
[Considerações de segurança arquiteturais]

## Evolução da Arquitetura

[Breve histórico de como a arquitetura evoluiu]
[Direções futuras planejadas]

## Referências

- [ADRs completos](../adr/README.md)
- [Padrões de Comunicação](communication-patterns.md)
```

#### 5. Padrões de Comunicação: `meta/architecture/communication-patterns.md`

```markdown
# Padrões de Comunicação

> Última atualização: [Data]
>
> Este documento descreve como os componentes do sistema se comunicam,
> incluindo protocolos, padrões e contratos.

## Visão Geral

[Descrição geral da estratégia de comunicação]

## Padrões de Comunicação Utilizados

### Comunicação Síncrona

#### REST APIs

**Uso**: [Quando e onde REST é usado]
**Padrão**: [Convenções seguidas]
**Autenticação**: [Estratégia de auth]
**Versionamento**: [Como APIs são versionadas]

**Decisões Relacionadas**:
- [ADR 00XX: Use REST for Public APIs](../adr/00XX-use-rest-for-public-apis.md)

**Exemplo de Request/Response**:
```http
GET /api/v1/resources/123
Authorization: Bearer <token>

200 OK
{
  "id": "123",
  "name": "Resource Name",
  ...
}
```

#### gRPC

[Se aplicável - seguir estrutura similar]

### Comunicação Assíncrona

#### Message Queue (ex: RabbitMQ, Kafka)

**Uso**: [Quando e onde messaging é usado]
**Padrões**: [Pub/Sub, Work Queues, etc.]
**Garantias**: [At-least-once, exactly-once, etc.]
**Formato de Mensagens**: [JSON, Protobuf, etc.]

**Decisões Relacionadas**:
- [ADR 00XX: Use Kafka for Event Streaming](../adr/00XX-use-kafka.md)

**Exemplo de Mensagem**:
```json
{
  "event_type": "user.created",
  "timestamp": "2024-01-15T10:30:00Z",
  "payload": {
    "user_id": "123",
    ...
  }
}
```

## Mapa de Comunicação entre Componentes

### Matriz de Comunicação

| De / Para | Componente A | Componente B | Componente C |
|-----------|--------------|--------------|--------------|
| **Componente A** | - | REST (sync) | Events (async) |
| **Componente B** | REST (sync) | - | gRPC (sync) |
| **Componente C** | Events (async) | gRPC (sync) | - |

### Diagramas de Sequência

#### Fluxo: [Nome do Fluxo Importante]

```
[Incluir diagrama de sequência - Mermaid ou ASCII]
```

## Contratos e Schemas

### API Contracts

[Como contratos são definidos e mantidos]
[Links para OpenAPI/Swagger specs se disponível]

### Event Schemas

[Como schemas de eventos são definidos]
[Registry de schemas se usado]

## Resiliência e Tratamento de Falhas

### Circuit Breakers

**Implementação**: [Biblioteca/ferramenta usada]
**Configuração**: [Thresholds, timeouts]
**Componentes protegidos**: [Lista]

### Retries

**Estratégia**: [Exponential backoff, fixed, etc.]
**Limites**: [Max retries, timeout total]

### Fallbacks

[Como fallbacks são implementados quando comunicação falha]

## Observabilidade de Comunicação

### Traces Distribuídos

**Ferramenta**: [Ex: OpenTelemetry, Jaeger]
**Propagação**: [Como trace context é propagado]

### Métricas de Comunicação

- Latência de requests (p50, p95, p99)
- Taxa de erro
- Throughput
- [Outras métricas relevantes]

## Segurança na Comunicação

### Autenticação

[Estratégias de autenticação entre componentes]

### Autorização

[Como permissões são verificadas]

### Criptografia

[TLS/SSL, encryption at rest, etc.]

## Decisões Relacionadas

- [ADR 00XX: Communication Decision 1](../adr/00XX-....md)
- [ADR 00XX: Communication Decision 2](../adr/00XX-....md)

## Evolução

[Como padrões de comunicação evoluíram]
[Mudanças planejadas]

## Referências

- [Visão Geral da Arquitetura](system-overview.md)
- [ADRs](../adr/README.md)
```

## Garantia de Qualidade

### Critérios de Validação dos ADRs

- [ ] **Contexto claro**: Cada ADR explica o problema/situação que motivou a decisão
- [ ] **Decisão explícita**: O que foi decidido está declarado claramente
- [ ] **Alternativas documentadas**: Outras opções consideradas estão listadas com prós/contras
- [ ] **Consequências honestas**: Impactos positivos E negativos estão documentados
- [ ] **Trade-offs explícitos**: O que foi sacrificado em favor de quê está claro
- [ ] **Status correto**: Status reflete realidade atual (Ativa, Superseded, Deprecated)
- [ ] **Validação**: Usuário confirmou contexto, alternativas e consequências

### Validação da Documentação Complementar

- [ ] **system-overview.md** captura componentes principais e suas relações
- [ ] **communication-patterns.md** documenta todos os tipos de comunicação usados
- [ ] Diagramas ajudam visualização (quando aplicável)
- [ ] Links entre ADRs e documentação arquitetural funcionam
- [ ] Documentação reflete estado atual do sistema

### Qualidade Geral

- [ ] Numeração sequencial dos ADRs está correta
- [ ] Índice no README.md está completo e organizado
- [ ] Linguagem é clara e não ambígua
- [ ] Decisões são específicas ao projeto, não genéricas
- [ ] Template está disponível para novos ADRs

## Estratégia de Execução

1. **Análise Profunda**: Leia toda documentação e código antes de identificar decisões
2. **Foco em Decisões Significativas**: Nem toda escolha técnica merece um ADR - foque nas que têm impacto duradouro
3. **Capture o Contexto Real**: Use perguntas ao usuário para entender o "por quê" verdadeiro
4. **Honestidade sobre Consequências**: Documente problemas e trade-offs, não apenas sucessos
5. **Organizção Lógica**: Numere ADRs em ordem cronológica ou lógica de dependência
6. **Complementaridade**: system-overview e communication-patterns devem complementar ADRs, não duplicar

## O que Merece um ADR?

### Merece ADR (exemplos):
- Escolha de linguagem, framework ou banco de dados
- Decisão de padrão arquitetural (monolito vs microserviços)
- Escolha de protocolo de comunicação crítico
- Estratégia de deploy e infraestrutura
- Decisões de segurança fundamentais
- Mudanças arquiteturais significativas

### NÃO merece ADR (exemplos):
- Escolha de biblioteca utilitária pequena
- Convenção de nomenclatura específica
- Configuração de ferramenta de desenvolvimento
- Decisão tática e reversível facilmente

**Regra geral**: Se a reversão da decisão seria custosa ou complexa, provavelmente merece um ADR.

## Tratamento de Casos Especiais

**Se houver ADRs existentes:**
- Não renumere, continue a numeração existente
- Revise ADRs antigos e atualize status se necessário
- Identifique decisões não documentadas e crie ADRs para elas

**Se o projeto for muito novo:**
- Documente as decisões iniciais (escolhas de stack, arquitetura)
- Marque claramente que são decisões iniciais, sujeitas a evolução
- Foque em capturar a intenção e critérios de avaliação

**Se houver decisões implícitas/acidentais:**
- Pergunte ao usuário se devem ser formalizadas
- Se sim, documente como "ratificação" de decisão existente
- Se não, considere se é dívida técnica a ser endereçada

## Critérios de Sucesso

A documentação ADR gerada deve permitir:
- **Novos membros** entenderem por que o sistema é como é
- **Decisões futuras** serem tomadas com conhecimento das decisões passadas
- **Refatorações** serem planejadas entendendo as consequências originais
- **Revisão de decisões** verificar se contexto mudou e decisão ainda é válida
- **Comunicação** entre equipes sobre escolhas arquiteturais

## Notas Importantes

- **Seja histórico quando apropriado**: ADRs podem capturar decisões passadas mesmo que não sejam mais ativas
- **Numere cronologicamente**: Novos ADRs sempre recebem próximo número, nunca reordene
- **Não delete ADRs**: Marque como Superseded ou Deprecated, mas mantenha o histórico
- **Capture o contexto da época**: Decisão pode parecer estranha hoje, mas fez sentido no contexto original
- **Trade-offs são normais**: Toda decisão tem aspectos negativos, documente-os honestamente

Lembre-se: ADRs são um registro histórico que conta a história do projeto através de suas decisões arquiteturais. Eles devem ser precisos, honestos e úteis para decisões futuras.
