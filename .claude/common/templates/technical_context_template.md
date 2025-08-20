# Context Architecture Template
*A strategic framework for designing documentation and context systems that enable AI-powered development*

---

## Purpose of This Template

This template helps software development teams design their **Context Architecture** - the systematic approach to organizing, structuring, and maintaining all project information so that both humans and AI can work effectively with your codebase.

**Use this template to:**
- Define what documentation and context your project needs
- Structure information for optimal AI consumption
- Create sustainable knowledge management systems
- Enable effective human-AI collaboration
- Scale development team productivity

---

## Project Context Profile

### Basic Project Information

**Project Name:** `[Your Project Name]`

**Project Type:** 
- [ ] Web Application
- [ ] Mobile Application  
- [ ] API/Backend Service
- [ ] Desktop Application
- [ ] Library/Framework
- [ ] CLI Tool
- [ ] Infrastructure/DevOps
- [ ] Other: `__________`

**Technology Stack:**
- **Primary Language:** `__________`
- **Framework/Runtime:** `__________`
- **Database:** `__________`
- **Cloud/Infrastructure:** `__________`
- **Key Dependencies:** `__________`

**Team Structure:**
- **Team Size:** `____` developers
- **Experience Level:** 
  - [ ] Junior (0-2 years)
  - [ ] Mid-level (2-5 years)
  - [ ] Senior (5+ years)
  - [ ] Mixed team
- **AI Tool Usage:**
  - [ ] GitHub Copilot
  - [ ] Claude/ChatGPT for development
  - [ ] Cursor/Windsurf
  - [ ] Other: `__________`

**Development Constraints:**
- [ ] High compliance requirements (SOX, HIPAA, etc.)
- [ ] Legacy system integration
- [ ] Performance-critical application
- [ ] Rapid prototyping/MVP focus
- [ ] Long-term maintenance (5+ years)
- [ ] Multiple team collaboration
- [ ] External developer onboarding

---

## Context Architecture Design

**IMPORTANT: Create a multi-file structure with an index.md that links to separate files for each layer. Do NOT create one large file.**

**Implementation Approach:**
1. **First**: Create `index.md` with the project profile and layer links
2. **Then**: Create individual files for each layer as needed
3. **Finally**: Ensure all links in the index work correctly

**File Naming Convention:**
- Use UPPERCASE for generic documentation files (e.g., `CODEBASE_GUIDE.md`)
- Use lowercase for project-specific files (e.g., `project_charter.md`) 
- Keep filenames descriptive and consistent

### Create an Index File First

**Create: `index.md` (or `technical_context.md`)**
```markdown
## Project Context Profile

### Basic Project Information
[Include the project profile information here]

---

## Layer 1: Core Project Context

- [Project Charter](project_charter.md)
- [Architecture Decision Records](adr/)

## Layer 2: AI-Optimized Context Files

- [AI Development Guide](CLAUDE.meta.md) - Example CLAUDE.md file for project level  
- [Codebase Navigation Guide](CODEBASE_GUIDE.md)

## Layer 3: Domain-Specific Context

- [Business Logic Documentation](BUSINESS_LOGIC.md)
- [API Specifications](API_SPECIFICATION.md)

## Layer 4: Development Workflow Context

- [Development Workflow Guide](CONTRIBUTING.md)
- [Troubleshooting Guide](TROUBLESHOOTING.md)

[Include remaining sections: Context Maintenance Strategy, AI Integration Guidelines, Success Metrics, Implementation Validation]
```

### Layer 1: Core Project Context

**Create: `project_charter.md`**
```markdown
# Project Charter: [Project Name]

## Vision Statement
What does this project aim to achieve? Why does it exist?

## Success Criteria
How will you know if this project is successful?

## Scope Boundaries
What is explicitly IN scope and OUT of scope?

## Key Stakeholders
Who are the primary users, sponsors, and decision makers?

## Technical Constraints
What are the non-negotiable technical requirements?
```

**Create: `adr/` directory with individual ADR files**
```markdown
File: `adr/001-[decision-name].md`
Purpose: Context for why technical decisions were made

Template per decision:
# ADR-001: [Decision Title]

## Context
What circumstances led to this decision?

## Decision
What did we decide?

## Rationale
Why did we choose this approach?

## Consequences
What are the positive and negative impacts?

## Alternatives Considered
What other options did we evaluate?
```

### Layer 2: AI-Optimized Context Files

**Create: `CLAUDE.meta.md` (AI Development Guide)**
```markdown
# AI Development Guide

## Code Style Preferences
- Preferred patterns and conventions
- Code organization principles
- Naming conventions
- Comment style requirements

## Testing Approach
- Testing framework used
- Test file structure and naming
- Coverage requirements
- Test data management

## Common Patterns
- Frequently used design patterns
- Project-specific abstractions
- Error handling conventions
- Logging and monitoring patterns

## Gotchas and Anti-patterns
- Common mistakes to avoid
- Performance considerations
- Security requirements
- Integration pitfalls
```

**Create: `CODEBASE_GUIDE.md`**
```markdown
# Codebase Navigation Guide

## Directory Structure
```
/src
  /components  # Reusable UI components
  /services    # Business logic layer
  /utils       # Helper functions
/tests         # Test files
/docs          # Documentation
```

## Key Files and Their Purpose
- `src/main.js` - Application entry point
- `src/config.js` - Configuration management
- `src/router.js` - Route definitions

## Data Flow Patterns
How data moves through the application

## Integration Points
External services, APIs, databases

## Deployment Architecture
How the application is deployed and scaled
```

### Layer 3: Domain-Specific Context

**Create: `BUSINESS_LOGIC.md` (CONDITIONAL)**
```markdown
Required if:
- [ ] Complex business rules exist
- [ ] Domain expertise needed
- [ ] Regulatory compliance involved
- [ ] Non-obvious business logic

# Business Logic Documentation

## Domain Concepts
Key business entities and their relationships

## Business Rules
Detailed explanation of business logic

## Validation Rules
Data validation requirements and rationale

## Workflow Processes
Step-by-step business processes

## Edge Cases
Known edge cases and how to handle them
```

**Create: `API_SPECIFICATION.md` (CONDITIONAL)**
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

### Layer 4: Development Workflow Context

**Create: `CONTRIBUTING.md` (Development Workflow Guide)**
```markdown
# Development Workflow

## Branch Strategy
Git workflow and branching conventions

## Code Review Process
Review requirements and criteria

## Testing Requirements
What tests are required before merging

## Deployment Process
How code gets from development to production

## Environment Setup
Local development environment setup

## Debugging Guide
Common debugging scenarios and tools
```

**Create: `TROUBLESHOOTING.md`**
```markdown
# Troubleshooting Guide

## Common Development Issues
Frequently encountered problems and solutions

## Environment-Specific Issues
Problems specific to local/staging/production

## Performance Issues
Known performance bottlenecks and optimizations

## Integration Issues
Third-party service integration problems

## Emergency Procedures
Critical issue response procedures
```

---

## Context Maintenance Strategy

### Ownership and Responsibility

**Documentation Owner Assignment:**
- **Project Charter:** `[Role/Person]` - Updated when major scope changes
- **ADRs:** `[Role/Person]` - Added for significant architectural decisions
- **AI Development Guide:** `[Role/Person]` - Updated as coding standards evolve
- **Business Logic:** `[Role/Person]` - Updated when business rules change
- **API Specs:** `[Role/Person]` - Updated with API changes

### Update Triggers

**When to update documentation:**
- [ ] New major features added
- [ ] Architecture decisions made
- [ ] Business rules change
- [ ] Performance issues discovered
- [ ] Security requirements updated
- [ ] Team composition changes
- [ ] Technology stack updates

### Quality Assurance Process

**Documentation Review Checklist:**
- [ ] Information is current and accurate
- [ ] Examples work and are tested
- [ ] Language is clear and unambiguous
- [ ] AI can understand and use the information
- [ ] Human developers find it helpful
- [ ] Links and references are valid

---

## AI Integration Guidelines

### Context File Organization

**Recommended file structure for AI consumption:**
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