# Template de Arquitetura de Contexto
*Um framework estratégico para projetar documentação e sistemas de contexto que habilitam desenvolvimento orientado por IA*

---

## Propósito deste Template

Este template ajuda equipes de desenvolvimento de software a projetar sua **Arquitetura de Contexto** - a abordagem sistemática para organizar, estruturar e manter todas as informações do projeto para que tanto humanos quanto IA possam trabalhar efetivamente com seu código.

**Use este template para:**
- Definir que documentação e contexto seu projeto precisa
- Estruturar informação para consumo otimizado pela IA
- Criar sistemas sustentáveis de gestão de conhecimento
- Habilitar colaboração efetiva humano-IA
- Escalar a produtividade da equipe de desenvolvimento

---

## Perfil do Contexto do Projeto

### Informações Básicas do Projeto

**Nome do Projeto:** `[Nome do Seu Projeto]`

**Tipo do Projeto:** 
- [ ] Aplicação Web
- [ ] Aplicação Mobile  
- [ ] API/Serviço Backend
- [ ] Aplicação Desktop
- [ ] Biblioteca/Framework
- [ ] Ferramenta CLI
- [ ] Infraestrutura/DevOps
- [ ] Outro: `__________`

**Stack Tecnológico:**
- **Linguagem Principal:** `__________`
- **Framework/Runtime:** `__________`
- **Banco de Dados:** `__________`
- **Nuvem/Infraestrutura:** `__________`
- **Dependências Principais:** `__________`

**Estrutura da Equipe:**
- **Tamanho da Equipe:** `____` desenvolvedores
- **Nível de Experiência:** 
  - [ ] Júnior (0-2 anos)
  - [ ] Intermediário (2-5 anos)
  - [ ] Sênior (5+ anos)
  - [ ] Equipe mista
- **Uso de Ferramentas IA:**
  - [ ] GitHub Copilot
  - [ ] Claude/ChatGPT para desenvolvimento
  - [ ] Cursor/Windsurf
  - [ ] Outro: `__________`

**Restrições de Desenvolvimento:**
- [ ] Altos requisitos de compliance (SOX, HIPAA, etc.)
- [ ] Integração com sistemas legados
- [ ] Aplicação crítica em performance
- [ ] Foco em prototipagem rápida/MVP
- [ ] Manutenção de longo prazo (5+ anos)
- [ ] Colaboração de múltiplas equipes
- [ ] Onboarding de desenvolvedores externos

---

## Design da Arquitetura de Contexto

**IMPORTANTE: Crie uma estrutura multi-arquivo com um index.md que faça links para arquivos separados para cada camada. NÃO crie um arquivo grande único.**

**Abordagem de Implementação:**
1. **Primeiro**: Crie `index.md` com o perfil do projeto e links das camadas
2. **Depois**: Crie arquivos individuais para cada camada conforme necessário
3. **Finalmente**: Certifique-se de que todos os links no índice funcionem corretamente

**Convenção de Nomeação de Arquivos:**
- Use MAIÚsCULAS para arquivos de documentação genéricos (ex.: `GUIA_CODEBASE.md`)
- Use minúsculas para arquivos específicos do projeto (ex.: `charter_projeto.md`) 
- Mantenha nomes de arquivo descritivos e consistentes

### Crie um Arquivo Índice Primeiro

**Crie: `index.md` (ou `contexto_tecnico.md`)**
```markdown
## Perfil do Contexto do Projeto

### Informações Básicas do Projeto
[Inclua as informações do perfil do projeto aqui]

---

## Camada 1: Contexto Central do Projeto

- [Charter do Projeto](charter_projeto.md)
- [Registros de Decisões Arquiteturais](adr/)

## Camada 2: Arquivos de Contexto Otimizados para IA

- [Guia de Desenvolvimento IA](CLAUDE.meta.md) - Exemplo de arquivo CLAUDE.md para nível de projeto  
- [Guia de Navegação do Codebase](GUIA_CODEBASE.md)

## Camada 3: Contexto Específico do Domínio

- [Documentação da Lógica de Negócio](LOGICA_NEGOCIO.md)
- [Especificações da API](ESPECIFICACAO_API.md)

## Camada 4: Contexto do Fluxo de Desenvolvimento

- [Guia de Fluxo de Desenvolvimento](CONTRIBUTING.md)
- [Guia de Solução de Problemas](TROUBLESHOOTING.md)

[Incluir seções restantes: Estratégia de Manutenção de Contexto, Diretrizes de Integração IA, Métricas de Sucesso, Validação de Implementação]
```

### Camada 1: Contexto Central do Projeto

**Crie: `charter_projeto.md`**
```markdown
# Charter do Projeto: [Nome do Projeto]

## Declaração de Visão
O que este projeto visa alcançar? Por que ele existe?

## Critérios de Sucesso
Como você saberá se este projeto é bem-sucedido?

## Limites do Escopo
O que está explicitamente DENTRO e FORA do escopo?

## Stakeholders Principais
Quem são os usuários primários, patrocinadores e tomadores de decisão?

## Restrições Técnicas
Quais são os requisitos técnicos inegociáveis?
```

**Crie: diretório `adr/` com arquivos ADR individuais**
```markdown
Arquivo: `adr/001-[nome-decisao].md`
Propósito: Contexto para por que decisões técnicas foram tomadas

Template por decisão:
# ADR-001: [Título da Decisão]

## Contexto
Que circunstâncias levaram a esta decisão?

## Decisão
O que decidimos?

## Justificativa
Por que escolhemos esta abordagem?

## Consequências
Quais são os impactos positivos e negativos?

## Alternativas Consideradas
Que outras opções avaliamos?
```

### Camada 2: Arquivos de Contexto Otimizados para IA

**Crie: `CLAUDE.meta.md` (Guia de Desenvolvimento IA)**
```markdown
# Guia de Desenvolvimento IA

## Preferências de Estilo de Código
- Padrões e convenções preferidos
- Princípios de organização do código
- Convenções de nomeação
- Requisitos de estilo de comentários

## Abordagem de Testes
- Framework de testes usado
- Estrutura e nomeação de arquivos de teste
- Requisitos de cobertura
- Gestão de dados de teste

## Padrões Comuns
- Padrões de design frequentemente usados
- Abstrações específicas do projeto
- Convenções de tratamento de erro
- Padrões de logging e monitoramento

## Pegadinhas e Anti-padrões
- Erros comuns a evitar
- Considerações de performance
- Requisitos de segurança
- Armadilhas de integração
```

**Crie: `GUIA_CODEBASE.md`**
```markdown
# Guia de Navegação do Codebase

## Estrutura de Diretórios
```
/src
  /components  # Componentes de UI reutilizáveis
  /services    # Camada de lógica de negócio
  /utils       # Funções auxiliares
/tests         # Arquivos de teste
/docs          # Documentação
```

## Arquivos Principais e Seu Propósito
- `src/main.js` - Ponto de entrada da aplicação
- `src/config.js` - Gestão de configuração
- `src/router.js` - Definições de rotas

## Padrões de Fluxo de Dados
Como os dados se movem pela aplicação

## Pontos de Integração
Serviços externos, APIs, bancos de dados

## Arquitetura de Deploy
Como a aplicação é implantada e escalada
```

### Camada 3: Contexto Específico do Domínio

**Crie: `LOGICA_NEGOCIO.md` (CONDICIONAL)**
```markdown
Necessário se:
- [ ] Existem regras de negócio complexas
- [ ] Expertise do domínio é necessária
- [ ] Compliance regulatório está envolvido
- [ ] Lógica de negócio não óbvia

# Documentação da Lógica de Negócio

## Conceitos do Domínio
Entidades de negócio principais e seus relacionamentos

## Regras de Negócio
Explicação detalhada da lógica de negócio

## Regras de Validação
Requisitos de validação de dados e justificativa

## Processos de Workflow
Processos de negócio passo a passo

## Casos Extremos
Casos extremos conhecidos e como lidar com eles
```

**Crie: `ESPECIFICACAO_API.md` (CONDICIONAL)**
```markdown
Required if:
- [ ] Building APIs for external consumption
- [ ] Complex integration patterns
- [ ] Multiple API versions
- [ ] Third-party integrations

# API Specification

## Authentication & Authorization
How to authenticate and what permissions exist

## Endpoint Documentation
Detailed endpoint descriptions with examples

## Data Models
Request/response schemas and validation rules

## Error Handling
Error codes, messages, and recovery strategies

## Rate Limiting & Performance
Usage limits and performance expectations
```

### Camada 4: Contexto do Fluxo de Desenvolvimento

**Crie: `CONTRIBUTING.md` (Guia de Fluxo de Desenvolvimento)**
```markdown
# Fluxo de Desenvolvimento

## Estratégia de Branch
Fluxo Git e convenções de branching

## Processo de Code Review
Requisitos e critérios de revisão

## Requisitos de Teste
Que testes são necessários antes do merge

## Processo de Deploy
Como o código vai do desenvolvimento para produção

## Configuração do Ambiente
Configuração do ambiente de desenvolvimento local

## Guia de Debugging
Cenários comuns de debugging e ferramentas
```

**Crie: `SOLUCAO_PROBLEMAS.md`**
```markdown
# Guia de Solução de Problemas

## Problemas Comuns de Desenvolvimento
Problemas encontrados frequentemente e soluções

## Problemas Específicos do Ambiente
Problemas específicos para local/staging/produção

## Problemas de Performance
Gargalos de performance conhecidos e otimizações

## Problemas de Integração
Problemas de integração com serviços de terceiros

## Procedimentos de Emergência
Procedimentos de resposta a problemas críticos
```

---

## Estratégia de Manutenção de Contexto

### Propriedade e Responsabilidade

**Atribuição de Proprietário da Documentação:**
- **Project Charter:** `[Role/Person]` - Updated when major scope changes
- **ADRs:** `[Role/Person]` - Added for significant architectural decisions
- **AI Development Guide:** `[Role/Person]` - Updated as coding standards evolve
- **Business Logic:** `[Role/Person]` - Updated when business rules change
- **API Specs:** `[Role/Person]` - Updated with API changes

### Gatilhos de Atualização

**Quando atualizar a documentação:**
- [ ] New major features added
- [ ] Architecture decisions made
- [ ] Business rules change
- [ ] Performance issues discovered
- [ ] Security requirements updated
- [ ] Team composition changes
- [ ] Technology stack updates

### Processo de Garantia de Qualidade

**Checklist de Revisão da Documentação:**
- [ ] Information is current and accurate
- [ ] Examples work and are tested
- [ ] Language is clear and unambiguous
- [ ] AI can understand and use the information
- [ ] Human developers find it helpful
- [ ] Links and references are valid

---

## Diretrizes de Integração com IA

### Organização de Arquivos de Contexto

**Estrutura de arquivos recomendada para consumo pela IA:**
```
/specs/technical/               # or /docs/context/
  index.md                     # Main index with links to all layers
  project_charter.md           # Layer 1: Core context
  /adr/                        # Layer 1: Architecture decisions
    001-database-choice.md
    002-authentication-strategy.md
  CLAUDE.meta.md              # Layer 2: AI development guide
  CODEBASE_GUIDE.md           # Layer 2: Navigation guide
  BUSINESS_LOGIC.md           # Layer 3: Domain knowledge
  API_SPECIFICATION.md        # Layer 3: API documentation
  CONTRIBUTING.md             # Layer 4: Development workflow
  TROUBLESHOOTING.md          # Layer 4: Issue resolution
```

**Key Benefits of This Structure:**
- **Modular**: Each file focuses on a specific concern
- **Linked**: Index file provides navigation and overview
- **Maintainable**: Updates target specific files, not one large document
- **AI-Friendly**: Clear file names and focused content improve AI understanding

### AI Tool Configuration

**For GitHub Copilot:**
- Ensure context files are in repository root or `/docs`
- Use clear, descriptive file names
- Include relevant examples and code snippets

**For Claude/ChatGPT Development:**
- Create consolidated context packages for complex discussions
- Maintain current context summaries for long development sessions
- Include relevant error logs and debugging context

**For Cursor/Windsurf:**
- Configure `.cursorrules` or equivalent with project-specific guidelines
- Reference key documentation files in AI instructions
- Maintain workspace-specific context configurations

### Context Compression Strategies

**For large projects, consider:**
- **Hierarchical documentation** - overview → detailed sections
- **Context summaries** - condensed versions of key information
- **Dynamic context loading** - context relevant to current work
- **Cross-references** - links between related documentation

---

## Success Metrics and Validation

### Quantitative Metrics

**Development Efficiency:**
- **Time to first contribution** for new team members
- **Code review cycle time** reduction
- **Bug resolution time** improvement
- **Feature development velocity** increase

**AI Effectiveness:**
- **AI suggestion acceptance rate** improvement
- **Code quality metrics** (test coverage, complexity, bugs)
- **Documentation usage** tracking and feedback
- **AI-generated code review** pass rates

### Qualitative Assessment

**Team Satisfaction Indicators:**
- [ ] Developers report faster onboarding
- [ ] AI tools provide more relevant suggestions
- [ ] Code reviews focus on logic rather than style/convention issues
- [ ] Less time spent explaining project context
- [ ] Reduced frustration with AI tool limitations

**Context Quality Indicators:**
- [ ] Documentation stays current without heroic effort
- [ ] New team members can contribute quickly
- [ ] AI tools understand project patterns and constraints
- [ ] Cross-team collaboration improves
- [ ] Technical debt decreases over time

---

## Implementation Checklist

### Phase 1: Foundation (Week 1-2)
- [ ] Complete Project Context Profile
- [ ] Create PROJECT_CHARTER.md
- [ ] Set up ADR structure and process
- [ ] Assign documentation ownership

### Phase 2: AI Optimization (Week 2-3)
- [ ] Create AI_DEVELOPMENT_GUIDE.md
- [ ] Create CODEBASE_GUIDE.md
- [ ] Configure AI tools with project context
- [ ] Test AI effectiveness with new context

### Phase 3: Domain Context (Week 3-4)
- [ ] Create domain-specific documentation as needed
- [ ] Document business logic and API specifications
- [ ] Create workflow and troubleshooting guides
- [ ] Validate context completeness

### Phase 4: Maintenance (Ongoing)
- [ ] Establish update triggers and processes
- [ ] Create quality assurance procedures
- [ ] Monitor and measure success metrics
- [ ] Iterate and improve based on feedback

---

## Customization Guidelines

### For Different Project Types

**API/Backend Services:**
- Emphasize API documentation and integration patterns
- Include comprehensive error handling documentation
- Document performance characteristics and scaling patterns

**Frontend Applications:**
- Focus on component architecture and UI patterns
- Include user experience guidelines and accessibility requirements
- Document state management and data flow patterns

**Libraries/Frameworks:**
- Prioritize usage examples and API documentation
- Include migration guides and breaking change documentation
- Document performance characteristics and compatibility requirements

**Enterprise Applications:**
- Emphasize compliance and security documentation
- Include detailed business process documentation
- Document integration patterns with enterprise systems

### For Different Team Contexts

**Small Teams (1-3 developers):**
- Focus on essential documentation only
- Combine multiple context types into fewer files
- Emphasize practical examples over comprehensive theory

**Large Teams (10+ developers):**
- Create detailed, specialized documentation
- Implement strict documentation governance
- Include comprehensive onboarding and cross-team collaboration guides

**Distributed Teams:**
- Emphasize asynchronous communication patterns
- Include detailed decision-making processes
- Document cultural and communication preferences

---

## Template Validation

This template should be reviewed and customized based on:
- **Project complexity and requirements**
- **Team size and experience level**
- **AI tool adoption and sophistication**
- **Organizational culture and constraints**
- **Industry-specific requirements**

Regular template updates should incorporate:
- **Lessons learned from implementation**
- **New AI tool capabilities and requirements**
- **Evolving development practices and patterns**
- **Team feedback and usage analytics**