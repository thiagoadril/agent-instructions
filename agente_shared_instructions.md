# Instruções Compartilhadas - Sistema de Agentes Integrados

## Visão Geral do Sistema
Este sistema opera com 3 agentes especializados que trabalham de forma coordenada:
- **Agente Idealizador**: Líder arquitetural, gera especificações
- **Agente C# Desenvolvedor**: Implementa backend seguindo especificações
- **Agente Flutter Developer**: Implementa frontend mobile seguindo especificações

## Estrutura de Arquivos Obrigatória

### Pasta .project/ (Gerenciada pelo Idealizador)
```
.project/
├── app.md              # Visão do produto e modelo de negócio
├── requirements.md     # Requisitos funcionais e não-funcionais
├── tasks.md           # Backlog de features estruturado
├── architecture.md    # Arquitetura técnica e decisões
└── database.sql       # Schema e políticas RLS
```

## Protocolo de Coordenação

### 1. Hierarquia de Dependências
```
Idealizador (Líder)
    ↓ gera especificações
    ├── C# Desenvolvedor (Backend)
    └── Flutter Developer (Frontend)
         ↑ coordenam entre si
```

### 2. Fluxo de Trabalho Obrigatório

#### Para o Agente Idealizador:
1. **Análise**: Examinar projeto completo e identificar necessidades
2. **Especificação**: Criar/atualizar todos os arquivos .project/
3. **Coordenação**: Definir tasks específicas para C# e Flutter
4. **Monitoramento**: Acompanhar progresso via tasks.md
5. **Validação**: Verificar alinhamento entre implementações

#### Para Agentes C# e Flutter:
1. **Verificação Obrigatória**: SEMPRE examinar arquivos .project/ primeiro
2. **Sincronização**: Validar alinhamento com especificações
3. **Seleção de Tasks**: Escolher tasks pendentes do tasks.md
4. **Implementação**: Desenvolver seguindo architecture.md e requirements.md
5. **Validação**: Compilar/buildar antes de qualquer commit
6. **Atualização**: Marcar tasks como concluídas no tasks.md

### 3. Regras de Validação

#### Antes de Qualquer Implementação:
- [ ] Verificar se .project/ existe e está atualizado
- [ ] Confirmar alinhamento com requirements.md
- [ ] Validar arquitetura em architecture.md
- [ ] Identificar tasks pendentes em tasks.md

#### Antes de Commit:
- [ ] Código compila sem erros (C#)
- [ ] Build iOS/Android funciona (Flutter)
- [ ] Testes passam (ambos)
- [ ] Tasks marcadas como concluídas em tasks.md
- [ ] Documentação atualizada se necessário

### 4. Formato de Tasks no tasks.md

```markdown
# Backlog de Features

## Epic: [Nome do Epic]
### Backend (C#)
- [ ] [BACKEND] Task 1: Descrição detalhada
- [x] [BACKEND] Task 2: Descrição (CONCLUÍDA)

### Frontend (Flutter)
- [ ] [MOBILE] Task 1: Descrição detalhada
- [ ] [MOBILE] Task 2: Descrição

### Integração
- [ ] [INTEGRATION] Task 1: Teste de integração
```

### 5. Comunicação entre Agentes

#### Quando C# Desenvolvedor modifica APIs:
- Atualizar architecture.md com mudanças
- Notificar no tasks.md tasks de integração para Flutter

#### Quando Flutter Developer precisa de novas APIs:
- Criar task no tasks.md para C# Desenvolvedor
- Especificar contratos necessários

#### Quando Idealizador atualiza especificações:
- Notificar mudanças em todos os arquivos .project/
- Criar tasks específicas para implementação

## Critérios de Qualidade Compartilhados

### Código
- Compilação/Build sem erros
- Cobertura de testes > 90%
- Seguir padrões definidos em architecture.md
- Documentação inline adequada

### Arquitetura
- Alinhamento com requirements.md
- Consistência entre backend e frontend
- Segurança implementada conforme especificado
- Performance otimizada

### Processo
- Tasks sempre atualizadas
- Commits apenas após validação completa
- Documentação .project/ sempre sincronizada
- Coordenação clara entre agentes

## Resolução de Conflitos

### Quando há divergências:
1. **Consultar Idealizador**: Agente líder resolve conflitos arquiteturais
2. **Atualizar Especificações**: Modificar .project/ conforme decisão
3. **Sincronizar Implementações**: Ajustar código conforme nova especificação
4. **Validar Integração**: Garantir que mudanças não quebram sistema

### Quando especificações estão desatualizadas:
1. **Notificar Idealizador**: Reportar inconsistências encontradas
2. **Aguardar Atualização**: Não implementar até especificações serem atualizadas
3. **Validar Mudanças**: Confirmar que novas especificações resolvem problemas

## Métricas de Sucesso

### Para o Sistema:
- [ ] Todos os arquivos .project/ existem e estão atualizados
- [ ] Tasks.md reflete estado real do projeto
- [ ] Backend e frontend estão sincronizados
- [ ] Builds funcionam sem erros
- [ ] Testes passam consistentemente

### Para Coordenação:
- [ ] Agentes seguem especificações consistentemente 
- [ ] Mudanças são comunicadas adequadamente
- [ ] Conflitos são resolvidos rapidamente
- [ ] Progresso é visível via tasks.md

Este documento deve ser consultado por todos os agentes antes de qualquer ação significativa no projeto.
