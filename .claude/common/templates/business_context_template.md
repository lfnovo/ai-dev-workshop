# Template de Arquitetura de Contexto de Negócios
*Framework estratégico para organizar conhecimento de negócios e habilitar desenvolvimento de produtos orientado por IA e sucesso do cliente*

---

## Propósito deste Template

Este template ajuda equipes de produto a projetar sua **Arquitetura de Contexto de Negócios** - a abordagem sistemática para organizar, estruturar e manter todo conhecimento de negócios para que a IA possa entender seus clientes, produto e mercado tão bem quanto os melhores membros da sua equipe.

**Use este template para:**
- Criar inteligência de negócios acessível à IA
- Permitir que a IA tome decisões de produto contextualmente apropriadas
- Escalar conhecimento institucional entre equipes
- Melhorar a experiência do cliente através de personalização com IA
- Acelerar a produtividade de novos membros da equipe

---

## Perfil do Contexto de Negócios

### Fundamentos da Empresa e Produto

**Visão Geral da Empresa:**
- **Nome da Empresa:** `[Sua Empresa]`
- **Indústria:** `__________`
- **Estágio da Empresa:** 
  - [ ] Startup (Pré-Product Market Fit)
  - [ ] Crescimento (Pós-PMF, Escalando)
  - [ ] Enterprise (Madura, Múltiplos Produtos)
  - [ ] Legacy (Estabelecida, Otimizando)

**Informações do Produto:**
- **Produto Principal:** `__________`
- **Categoria do Produto:** `__________`
- **Tamanho do Mercado Alvo:** `__________`
- **Modelo de Negócios:** 
  - [ ] Assinatura SaaS
  - [ ] Marketplace
  - [ ] E-commerce
  - [ ] Freemium
  - [ ] Licenciamento Enterprise
  - [ ] Outro: `__________`

**Receita e Escala:**
- **Faixa de Receita Anual:** `R$________`
- **Número de Clientes:** `________`
- **Tamanho da Equipe:** `____` pessoas
- **Métricas Primárias de Crescimento:** `__________`

---

## Design da Arquitetura de Contexto de Negócios

**IMPORTANTE: Crie uma estrutura multi-arquivo com um index.md que faça links para arquivos separados para cada camada. NÃO crie um arquivo grande único.**

**Abordagem de Implementação:**
1. **Primeiro**: Crie `index.md` com o perfil de negócios e links das camadas
2. **Depois**: Crie arquivos individuais para cada camada conforme necessário
3. **Finalmente**: Certifique-se de que todos os links no índice funcionem corretamente

**Convenção de Nomeação de Arquivos:**
- Use MAIÚsCULAS para arquivos de documentação de negócios genéricos (ex.: `PERSONAS_CLIENTES.md`)
- Use minúsculas para arquivos específicos do negócio (ex.: `perfil_negocio.md`) 
- Mantenha nomes de arquivo descritivos e focados no negócio

### Crie um Arquivo Índice Primeiro

**Crie: `index.md` (ou `contexto_negocio.md`)**
```markdown
## Perfil do Contexto de Negócios

### Fundamentos da Empresa e Produto
[Inclua as informações do perfil de negócios aqui]

---

## Camada 1: Arquitetura de Contexto do Cliente

- [Personas dos Clientes](PERSONAS_CLIENTES.md)
- [Jornada do Cliente](JORNADA_CLIENTE.md)
- [Voz do Cliente](VOZ_CLIENTE.md)

## Camada 2: Arquitetura de Contexto do Produto

- [Estratégia do Produto](ESTRATEGIA_PRODUTO.md)
- [Catálogo de Funcionalidades](CATALOGO_FUNCIONALIDADES.md)
- [Métricas do Produto](METRICAS_PRODUTO.md)

## Camada 3: Contexto de Mercado e Competitivo

- [Panorama Competitivo](PANORAMA_COMPETITIVO.md)
- [Tendências da Indústria](TENDENCIAS_INDUSTRIA.md)

## Camada 4: Contexto Operacional de Negócios

- [Processo de Vendas](PROCESSO_VENDAS.md)
- [Framework de Mensagens](FRAMEWORK_MENSAGENS.md)
- [Diretrizes de Comunicação com Cliente](COMUNICACAO_CLIENTE.md)

[Incluir seções restantes: Integração de Contexto, Medição de Sucesso, Estratégia de Implementação]
```

## Camada 1: Arquitetura de Contexto do Cliente

### Framework de Inteligência do Cliente

**Crie: `PERSONAS_CLIENTES.md`**
```markdown
# Personas dos Clientes

## Persona Principal: [Nome da Persona]
### Demografia
- Cargo/Título: [ex.: Gerente de Marketing]
- Tamanho da Empresa: [ex.: 50-200 funcionários]
- Indústria: [ex.: SaaS, E-commerce]
- Nível de Experiência: [ex.: 2-5 anos na função]

### Objetivos e Motivações
- Objetivos Primários: O que eles estão tentando alcançar?
- Métricas de Sucesso: Como eles medem o sucesso?
- Aspirações de Carreira: O que os motiva profissionalmente?

### Pontos de Dor e Desafios
- Processo Atual: Como eles resolvem isso hoje?
- Pontos de Atrito: Onde eles têm dificuldades?
- Restrições: O que limita suas opções?

### Contexto Tecnológico
- Ferramentas Usadas: Stack de software atual
- Conforto Técnico: Quão técnicos eles são?
- Processo de Decisão: Como eles avaliam soluções?

### Preferências de Comunicação
- Canais Preferidos: Email, Slack, telefone, etc.
- Estilo de Linguagem: Formal, casual, técnico
- Densidade de Informação: Resumos breves vs análise detalhada

### Notas de Interação com IA
- Como a IA deve se comunicar com esta persona?
- Que nível de detalhe eles preferem?
- Quais tópicos a IA deve evitar ou enfatizar?
```

**Crie: `JORNADA_CLIENTE.md`**
```markdown
# Mapa da Jornada do Cliente

## Estágio de Conscientização
### Eventos Gatilho
O que faz os clientes começarem a procurar soluções?

### Fontes de Informação
Onde eles pesquisam soluções?

### Questões Chave
O que eles estão tentando entender?

### Critérios de Sucesso
Como eles avaliam se uma solução pode funcionar?

## Estágio de Avaliação
### Critérios de Avaliação
Quais fatores eles consideram mais importantes?

### Tomadores de Decisão
Quem influencia a decisão de compra?

### Objeções Comuns
Quais preocupações tipicamente surgem?

### Pontos de Comprovação
Que evidência eles precisam ver?

## Estágio de Onboarding
### Marcos de Primeiro Sucesso
O que precisa acontecer para eles se sentirem bem-sucedidos?

### Pontos de Confusão Comuns
Onde novos clientes tipicamente têm dificuldades?

### Padrões de Adoção
Como clientes bem-sucedidos tipicamente usam o produto?

## Estágio de Crescimento
### Oportunidades de Expansão
Como os clientes tipicamente aumentam seu uso?

### Casos de Uso Avançados
Que fluxos sofisticados os power users desenvolvem?

### Indicadores de Sucesso
Quais comportamentos indicam um cliente próspero?

## Padrões de Retenção/Churn
### Indicadores de Risco de Churn
Sinais precoces de insatisfação do cliente

### Estratégias de Recuperação
Como reengajar clientes em risco

### Motivadores de Renovação
O que motiva clientes a continuar/expandir?
```

### Inteligência de Feedback do Cliente

**Crie: `VOZ_CLIENTE.md`**
```markdown
# Inteligência da Voz do Cliente

## Temas de Elogio Comuns
O que os clientes consistentemente amam no produto?

## Reclamações Frequentes
Quais problemas surgem repetidamente no suporte/feedback?

## Padrões de Solicitação de Funcionalidades
Quais melhorias os clientes solicitam com mais frequência?

## Comparações Competitivas
Como os clientes nos comparam às alternativas?

## Linguagem e Terminologia
- Como os clientes descrevem nosso produto?
- Que termos da indústria eles usam?
- Que jargão interno a IA deve evitar?

## Padrões de Comunicação
- Preferências de comunicação formal vs casual
- Expectativas de tempo de resposta por tipo de cliente
- Gatilhos e preferências de escalonamento
```

---

## Camada 2: Arquitetura de Contexto do Produto

### Framework de Inteligência do Produto

**Crie: `ESTRATEGIA_PRODUTO.md`**
```markdown
# Estratégia do Produto

## Visão e Missão
### Visão do Produto
Para onde o produto está indo em 2-3 anos?

### Declaração de Missão
Que problema o produto resolve?

### Definição de Sucesso
Como você mede o sucesso do produto?

## Posição no Mercado
### Panorama Competitivo
- Concorrentes Diretos: [Lista e breve descrição]
- Concorrentes Indiretos: [Soluções alternativas]
- Vantagens Competitivas: [O que diferencia você]

### Market Trends
- Industry Evolution: How is the market changing?
- Technology Trends: What tech trends affect the product?
- Customer Behavior Changes: How are users evolving?

## Strategic Priorities
### Current Quarter Focus
What are the top 3 product priorities?

### Annual Objectives
What must be achieved this year?

### Future Roadmap Themes
What major capabilities are planned?

## Product Principles
### Design Principles
What guides product design decisions?

### Trade-off Framework
How do you prioritize competing demands?

### Quality Standards
What level of quality is required?
```

**Create: `FEATURE_CATALOG.md`**
```markdown
# Feature Catalog

## Core Features
### [Feature Name]
**Purpose:** Why does this feature exist?
**User Benefit:** What value does it provide?
**Usage Patterns:** How do customers typically use it?
**Success Metrics:** How do you measure feature success?
**Limitations:** What can't it do?
**Common Issues:** What problems do users face?
**AI Considerations:** How should AI discuss this feature?

## Advanced Features
[Same template as above for sophisticated capabilities]

## Experimental Features
[Features in beta or testing phases]

## Deprecated Features
[Features being phased out or removed]

## Integration Capabilities
### Third-party Integrations
What external tools does the product connect with?

### API Capabilities
What can developers build with your APIs?

### Data Import/Export
How do customers get data in and out?
```

### Product Performance Intelligence

**Create: `PRODUCT_METRICS.md`**
```markdown
# Product Metrics Framework

## User Engagement Metrics
- Daily/Monthly Active Users
- Feature Adoption Rates
- User Session Patterns
- Retention Curves

## Business Performance Metrics
- Revenue per Customer
- Customer Acquisition Cost
- Lifetime Value
- Churn Rates

## Product Quality Metrics
- Bug Report Trends
- Performance Benchmarks
- User Satisfaction Scores
- Support Ticket Volume

## Feature Performance
### High-Performing Features
Which features drive the most engagement/value?

### Underperforming Features
Which features need attention or improvement?

### Usage Correlation Patterns
Which features are used together successfully?
```

---

## Layer 3: Market and Competitive Context

### Market Intelligence Framework

**Create: `COMPETITIVE_LANDSCAPE.md` (CONDITIONAL)**
```markdown
Required if:
- [ ] Competitive market with multiple players
- [ ] Frequent competitive positioning needed
- [ ] Sales team needs competitive talking points
- [ ] Product decisions influenced by competitive moves

# Competitive Landscape

## Direct Competitors
### [Competitor Name]
**Strengths:** What do they do well?
**Weaknesses:** Where do they fall short?
**Positioning:** How do they market themselves?
**Pricing:** How do they price their solution?
**Customer Overlap:** Do you compete for the same customers?
**Differentiation:** How are you different/better?

## Competitive Positioning Framework
### Win/Loss Analysis
Why do you win deals? Why do you lose them?

### Competitive Messaging
How should AI position the product against competitors?

### Objection Handling
Common competitive objections and responses
```

**Create: `INDUSTRY_TRENDS.md`**
```markdown
# Industry and Market Trends

## Industry Evolution
### Current State
How would you describe the industry today?

### Emerging Trends
What changes are happening in the market?

### Future Predictions
Where is the industry heading?

## Technology Impact
### Disruptive Technologies
What technologies could change the landscape?

### Adoption Patterns
How quickly does the industry adopt new solutions?

## Regulatory Environment
### Current Regulations
What rules govern the industry?

### Compliance Requirements
What standards must products meet?

### Regulatory Trends
How might regulations change?
```

---

## Layer 4: Operational Business Context

### Sales and Marketing Intelligence

**Create: `SALES_PROCESS.md`**
```markdown
# Sales Process and Methodology

## Sales Methodology
### Sales Process Stages
1. Lead Qualification
2. Discovery Process
3. Solution Presentation
4. Negotiation
5. Closing

### Qualification Criteria
What makes a good lead/prospect?

### Common Sales Objections
- Price/Budget Concerns
- Feature/Capability Questions
- Competitive Comparisons
- Implementation Concerns

### Sales Enablement Materials
- Demo Scripts and Flows
- ROI/Business Case Templates
- Competitive Battle Cards
- Implementation Timelines

## Customer Success Patterns
### Onboarding Best Practices
How do successful customers get started?

### Expansion Opportunities
When and how do customers typically expand?

### Renewal Strategy
What ensures customers renew/continue?
```

**Create: `MESSAGING_FRAMEWORK.md`**
```markdown
# Messaging and Brand Framework

## Brand Voice and Tone
### Brand Personality
How should the brand sound and feel?

### Tone Guidelines
- Professional vs Casual
- Technical vs Accessible
- Confident vs Humble
- Formal vs Friendly

### Voice Characteristics
What makes your brand voice distinctive?

## Core Messaging
### Value Proposition
What's the primary value you deliver?

### Key Messages
What are the 3-5 most important things to communicate?

### Proof Points
What evidence supports your claims?

## Messaging by Audience
### Enterprise Customers
How do you message to large organizations?

### SMB Customers
How do you message to smaller businesses?

### Technical Buyers
How do you message to technical decision makers?

### Business Buyers
How do you message to business stakeholders?

## Content Guidelines
### Topics to Emphasize
What subjects should AI prioritize in communications?

### Topics to Avoid
What subjects should AI be careful about?

### Communication Style
How formal/informal should AI communications be?
```

---

## Context Integration and AI Optimization

### AI Interaction Guidelines

**Create: `CUSTOMER_COMMUNICATION.md`**
```markdown
# AI Customer Communication Guidelines

## Communication Principles
### Primary Objectives
- Solve customer problems efficiently
- Maintain brand voice and values
- Create positive customer experiences
- Escalate appropriately when needed

### Tone and Style
- Professional but approachable
- Confident but not arrogant
- Helpful and solution-oriented
- Empathetic to customer concerns

## Response Guidelines
### Information Accuracy
- Always provide accurate, up-to-date information
- Acknowledge limitations and uncertainties
- Direct to appropriate resources when needed

### Escalation Triggers
When should AI escalate to humans?
- Complex technical problems
- Billing or contract issues
- Customer expressing frustration
- Requests outside AI capabilities

### Privacy and Security
- What customer information can AI access?
- How should AI handle sensitive data?
- What topics require extra privacy consideration?

## Personalization Strategy
### Customer Segmentation
How should AI adapt communication by customer type?

### Context Utilization
How should AI use customer history and preferences?

### Relationship Building
How should AI contribute to long-term customer relationships?
```

### Success Measurement Framework

**Business Context Quality Metrics**
```markdown
File: `/business-context/measurement/QUALITY_METRICS.md`
Purpose: Measuring business context effectiveness

Template:
# Business Context Quality Metrics

## AI Performance Metrics
### Customer Interaction Quality
- Customer satisfaction with AI interactions
- Resolution rate for AI-handled inquiries
- Escalation rate to human agents
- Response accuracy and relevance

### Sales and Marketing Effectiveness
- Lead qualification accuracy
- Message consistency across channels
- Conversion rate improvements
- Customer feedback on AI interactions

## Business Impact Metrics
### Customer Success
- Faster customer onboarding
- Improved customer retention
- Increased customer satisfaction scores
- Reduced support ticket volume

### Team Productivity
- New team member ramp-up time
- Cross-functional collaboration effectiveness
- Consistent decision-making across teams
- Reduced time spent explaining context

## Context Health Metrics
### Information Currency
- How often is business context updated?
- Are customer insights current and relevant?
- Is competitive information up-to-date?

### Usage and Adoption
- How often do teams reference business context?
- Are AI systems effectively using context?
- Is context helping improve business outcomes?
```

---

## Business Context File Organization

### Recommended File Structure

**Business context file structure for optimal AI consumption:**
```
/specs/business/                 # or /docs/business-context/
  index.md                      # Main index with links to all layers
  CUSTOMER_PERSONAS.md          # Layer 1: Customer intelligence
  CUSTOMER_JOURNEY.md           # Layer 1: Customer lifecycle
  VOICE_OF_CUSTOMER.md          # Layer 1: Customer feedback
  PRODUCT_STRATEGY.md           # Layer 2: Product context
  FEATURE_CATALOG.md            # Layer 2: Feature details
  PRODUCT_METRICS.md            # Layer 2: Performance data
  COMPETITIVE_LANDSCAPE.md      # Layer 3: Market intelligence
  INDUSTRY_TRENDS.md            # Layer 3: Market evolution
  SALES_PROCESS.md              # Layer 4: Sales methodology
  MESSAGING_FRAMEWORK.md        # Layer 4: Brand guidelines
  CUSTOMER_COMMUNICATION.md     # Layer 4: AI interaction guide
```

**Key Benefits of This Business Structure:**
- **Customer-Centric**: Organizes information around customer understanding
- **Scalable**: Easy to update specific business areas without affecting others
- **AI-Accessible**: Clear naming and focused content for better AI comprehension
- **Cross-Functional**: Different teams can maintain their domain expertise
- **Actionable**: Provides concrete guidance for customer interactions and decisions

### Integration with Technical Documentation

**Cross-Reference Strategy:**
- Business context informs technical priorities and decisions
- Technical constraints influence business strategy and messaging
- Customer feedback drives both product and technical roadmaps
- AI systems can access both business and technical context for comprehensive understanding

---

## Implementation and Maintenance Strategy

### Ownership and Governance

**Context Ownership Matrix**
- **Customer Personas:** Product/Marketing - Quarterly review
- **Customer Journey:** Customer Success - As customer patterns evolve
- **Product Strategy:** Product Leadership - Semi-annual strategic reviews
- **Feature Catalog:** Product Management - Monthly updates
- **Competitive Analysis:** Marketing/Sales - Quarterly updates
- **Messaging Framework:** Marketing - As needed for campaigns

### Update Triggers and Processes

**When to Update Business Context:**
- [ ] New customer segment discovered
- [ ] Product feature launches or changes
- [ ] Competitive landscape shifts
- [ ] Customer feedback patterns change
- [ ] Business model or strategy evolution
- [ ] Market conditions or trends change
- [ ] Regulatory environment changes

### Quality Assurance Framework

**Business Context Review Checklist:**
- [ ] Information reflects current business reality
- [ ] Customer insights are based on recent data
- [ ] Competitive information is current and accurate
- [ ] AI can understand and apply the context
- [ ] Cross-functional teams can use effectively
- [ ] Privacy and compliance requirements met

---

## Customization Guidelines

### For Different Business Models

**B2B SaaS:**
- Emphasize enterprise sales processes and customer success
- Include detailed feature adoption and expansion patterns
- Focus on competitive differentiation and ROI messaging

**B2C E-commerce:**
- Emphasize customer behavior patterns and personalization
- Include seasonal trends and promotional strategies
- Focus on conversion optimization and customer lifetime value

**Marketplace Platforms:**
- Include both buyer and seller perspectives
- Document network effects and growth patterns
- Focus on trust, safety, and transaction optimization

**Freemium Products:**
- Document conversion paths from free to paid
- Include usage patterns that predict conversion
- Focus on value demonstration and upgrade triggers

### For Different Company Stages

**Early Stage (Pre-PMF):**
- Focus on customer discovery and validation
- Emphasize experimentation and learning
- Keep documentation lightweight but systematic

**Growth Stage (Post-PMF):**
- Emphasize scaling and optimization
- Include detailed customer segmentation
- Focus on repeatable processes and playbooks

**Enterprise Stage:**
- Include comprehensive competitive analysis
- Emphasize compliance and governance
- Focus on cross-functional coordination

---

## Template Validation and Evolution

This business context architecture should be regularly evaluated for:
- **Relevance:** Does it reflect current business reality?
- **Completeness:** Does it cover all critical business knowledge?
- **Usability:** Can teams and AI effectively use this context?
- **Impact:** Is it improving business outcomes?

Regular template updates should incorporate:
- **Customer feedback and behavior changes**
- **Market evolution and competitive dynamics**
- **Product development and strategic shifts**
- **AI capability improvements and new use cases**