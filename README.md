# README - Sistema de Agentes Integrados

## 📋 Visão Geral

Este diretório contém o sistema de agentes especializados para desenvolvimento de software, baseado na metodologia **Feature Driven Development (FDD)** e arquitetura enterprise. O sistema é composto por agentes que trabalham de forma coordenada e hierárquica para garantir qualidade, consistência e eficiência no desenvolvimento.

## 🏗️ Arquitetura do Sistema

### Agentes Especializados

| Agente | Responsabilidade | Papel |
|--------|------------------|-------|
| **Agente Idealizador** | Líder arquitetural e estratégico | Gera especificações, define arquitetura, coordena equipe |
| **Agente C# Desenvolvedor** | Implementação backend | Desenvolve APIs, serviços e infraestrutura .NET |
| **Agente Flutter Developer** | Implementação frontend mobile | Desenvolve aplicações mobile multiplataforma |

### Hierarquia de Coordenação

```
Idealizador (Líder Arquitetural)
    ↓ especifica e coordena
    ├── C# Desenvolvedor (Backend)
    └── Flutter Developer (Frontend)
         ↑ colaboram e sincronizam
```

## 📁 Estrutura de Arquivos

### Agentes Principais
- [`agente_csharp_idealizador.md`](./agente_csharp_idealizador.md) - Agente líder arquitetural
- [`agente_csharp_desenvolvedor.md`](./agente_csharp_desenvolvedor.md) - Agente desenvolvedor backend .NET
- [`agente_flutter_developer.md`](./agente_flutter_developer.md) - Agente desenvolvedor mobile Flutter

### Documentação Central
- [`agente_shared_instructions.md`](./agente_shared_instructions.md) - **Instruções compartilhadas obrigatórias**

## 🔧 Como Utilizar

### 1. Configuração Inicial

1. **Leia as instruções compartilhadas**: Todos os agentes DEVEM consultar `agente_shared_instructions.md` antes de qualquer ação
2. **Verifique a estrutura .project/**: Certifique-se de que os arquivos de especificação existem
3. **Identifique seu papel**: Determine qual agente você está utilizando

### 2. Fluxo de Trabalho

#### Para o Agente Idealizador:
```bash
1. Analisar requisitos do projeto
2. Criar/atualizar arquivos .project/
3. Definir tasks específicas
4. Coordenar implementações
5. Validar alinhamento
```

#### Para Agentes Desenvolvedores:
```bash
1. Verificar arquivos .project/ (OBRIGATÓRIO)
2. Sincronizar com especificações
3. Selecionar tasks pendentes
4. Implementar seguindo padrões
5. Validar e atualizar tasks
```

### 3. Estrutura .project/ Obrigatória

Todos os projetos DEVEM ter:

```
.project/
├── app.md              # Visão do produto
├── requirements.md     # Requisitos funcionais
├── tasks.md           # Backlog estruturado
├── architecture.md    # Arquitetura técnica
└── database.sql       # Schema do banco
```

## ⚡ Regras Críticas

### ✅ Validações Obrigatórias

**Antes de Implementar:**
- [ ] Verificar se .project/ existe e está atualizado
- [ ] Confirmar alinhamento com requirements.md
- [ ] Validar arquitetura em architecture.md
- [ ] Identificar tasks pendentes em tasks.md

**Antes de Commit:**
- [ ] Código compila sem erros
- [ ] Build funciona (iOS/Android para Flutter)
- [ ] Testes passam
- [ ] Tasks marcadas como concluídas
- [ ] Documentação atualizada

### 🚫 Proibições

- ❌ **NUNCA** implementar sem consultar especificações
- ❌ **NUNCA** fazer commit com código que não compila
- ❌ **NUNCA** ignorar a hierarquia de coordenação
- ❌ **NUNCA** modificar arquitetura sem aprovação do Idealizador

## 📊 Métricas de Qualidade

### Código
- ✅ Compilação/Build sem erros
- ✅ Cobertura de testes > 90%
- ✅ Padrões arquiteturais seguidos
- ✅ Documentação inline adequada

### Processo
- ✅ Tasks sempre atualizadas
- ✅ Especificações sincronizadas
- ✅ Coordenação clara entre agentes
- ✅ Resolução rápida de conflitos

## 🔄 Metodologia FDD

O sistema segue rigorosamente os princípios do **Feature Driven Development**:

1. **Desenvolver um Modelo Abrangente** (Idealizador)
2. **Construir uma Lista de Funcionalidades** (tasks.md)
3. **Planejar por Funcionalidade** (architecture.md)
4. **Detalhar por Funcionalidade** (requirements.md)
5. **Construir por Funcionalidade** (Desenvolvedores)

## 🆘 Resolução de Problemas

### Conflitos Arquiteturais
1. Consultar Agente Idealizador
2. Atualizar especificações .project/
3. Sincronizar implementações
4. Validar integração

### Especificações Desatualizadas
1. Notificar Idealizador
2. Aguardar atualização
3. Validar mudanças
4. Prosseguir com implementação

## 📚 Recursos Adicionais

- [Metodologia FDD](https://en.wikipedia.org/wiki/Feature-driven_development)
- [Clean Architecture](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html)
- [Domain Driven Design](https://martinfowler.com/bliki/DomainDrivenDesign.html)
- [CQRS Pattern](https://martinfowler.com/bliki/CQRS.html)

## 🎯 Princípios Fundamentais

> *"A excelência em IA não vem da complexidade, mas da precisão na modelagem de comportamento e conhecimento."*
> 
> *- Princípios de Design de Personas AGI*

### Valores Core
- **Qualidade**: Código sem bugs, sempre compilável
- **Coordenação**: Trabalho em equipe estruturado
- **Eficiência**: Metodologia FDD aplicada rigorosamente
- **Manutenibilidade**: Código limpo e bem documentado
- **Segurança**: Implementação de boas práticas desde o início

---

**⚠️ IMPORTANTE**: Este README deve ser consultado junto com `agente_shared_instructions.md` antes de qualquer ação significativa no projeto.

**📝 Última atualização**: Documento criado para padronizar o uso do sistema de agentes integrados.
