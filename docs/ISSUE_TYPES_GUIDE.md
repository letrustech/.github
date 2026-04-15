# Guia de Issue Types - letrustech/.github

Este documento descreve os tipos de issues padronizados para a organização letrustech e quando usar cada um.

## Tipos de Issues Disponíveis

### 🐞 Bug
**Quando usar:** Para reportar erros, comportamentos inesperados ou problemas no sistema.

**Exemplos:**
- Botão de login não responde ao ser clicado
- Erro 500 ao tentar salvar dados
- Interface quebrada em dispositivos móveis
- Funcionalidade que parou de funcionar após um deploy

**Campos do template:**
1. **Descrição do problema:** descreva o problema de forma clara
2. **Passos para reproduzir:** como replicar o erro
3. **Comportamento esperado:** o que deveria acontecer
4. **Prioridade:** P0 (Crítico), P1 (Alto), P2 (Médio), P3 (Baixo)

**Prioridades:**
- **P0 - Crítico**: Sistema fora do ar, perda de dados, segurança comprometida
- **P1 - Alto**: Funcionalidade importante completamente quebrada
- **P2 - Médio**: Problema que afeta alguns usuários ou cenários específicos
- **P3 - Baixo**: Problema menor, cosmético ou workaround disponível

---

### 📝 Feature
**Quando usar:** Para propor novas funcionalidades ou capacidades que não existem no sistema.

**Exemplos:**
- Adicionar autenticação via SSO
- Criar dashboard de métricas
- Implementar notificações por email
- Adicionar exportação de dados em PDF

**Campos principais:**
- Objetivo e valor da funcionalidade
- Proposta de como deve funcionar
- Impacto esperado e riscos potenciais
- Alternativas consideradas

**Prioridades:**
- **P0 - Crítico**: Bloqueador para negócio, perda de receita sem essa feature
- **P1 - Alto**: Importante para roadmap, demanda de clientes
- **P2 - Médio**: Desejável, melhora experiência mas não urgente
- **P3 - Baixo**: Nice to have, pode esperar

---

### � Story
**Quando usar:** Para unidades de trabalho com valor de negócio claro que serão estimadas em Planning Poker (Story Points).

**Exemplos:**
- Implementar checkout com pagamento PIX
- Criar painel de controle para administradores
- Integrar sistema com API externa
- Desenvolver workflow de aprovação de pedidos

**Campos principais:**
- Story: descrição da funcionalidade/capacidade do ponto de vista do usuário
- Contexto: por quê isso é importante
- Critérios de aceitação: como validar que está completo
- Notas técnicas: detalhes de implementação
- Testes: checklist de testes a serem implementados

**Quando usar Story vs Feature:**
- Use **Story** quando vai entrar em um sprint e precisa ser estimado
- Use **Feature** para ideias no backlog de longo prazo
- Na prática, Features viram Stories quando refinadas

**Story Points:** Estimado em Planning Poker (1, 2, 3, 5, 8, 13, 21)

---

### ⚙️ Technical Story
**Quando usar:** Para trabalho técnico que não entrega feature de produto, mas tem valor técnico/operacional mensurável.

**Exemplos por área:**

**Backend:**
- Refatorar módulo de pagamentos para reduzir complexidade
- Migrar ORM de Sequelize para Prisma
- Otimizar queries N+1 (de 5s para <500ms)
- Implementar cache distribuído Redis

**Frontend:**
- Migrar aplicação de React 17 para 18
- Otimizar bundle (reduzir de 800KB para <200KB)
- Refatorar state management (Redux → Zustand)
- Implementar code splitting e lazy loading

**IA/ML:**
- Re-treinar modelo com novos dados
- Otimizar pipeline de feature engineering
- Melhorar acurácia do modelo de 85% para 92%
- Migrar inferência para GPU

**Infra/SRE:**
- Implementar auto-scaling Kubernetes
- Configurar observabilidade distribuída
- Migrar banco de dados Aurora serverless
- Automatizar backup e recovery

**QA/Testes:**
- Implementar framework de testes E2E
- Aumentar coverage de 40% para 80%
- Setup de smoke tests em produção
- Criar pipeline de testes de performance

**Segurança:**
- Implementar autenticação MFA
- Auditar e corrigir 15 vulnerabilidades críticas
- Implementar OWASP security headers
- Setup de scanning automático de dependências

**Campos do template:**
1. **Descrição:**
   - Problema/Necessidade Técnica: problema ou debt a ser resolvido
   - Solução Proposta: abordagem técnica resumida
   - Critérios de Aceitação: como validar que está completo
2. **Notas Técnicas:** ferramentas, dependências, riscos técnicos, alternativas
3. **Testes:** checklist de testes a serem implementados

**Diferença de Story tradicional:**
- **Story**: Entrega valor para **usuário final** (nova feature/capacidade)
- **Technical Story**: Entrega valor **técnico** (performance, qualidade, manutenibilidade, custos)
- Ambos têm estrutura similar, mas o foco da descrição muda

**Diferença de Task:**
- **Technical Story**: Trabalho significativo que será **estimado e pontuado** → conta no DevLake
- **Task**: Subtarefa de uma Story ou trabalho pequeno sem pontuação → não conta no DevLake

**Story Points:** Estimado em Planning Poker baseado em complexidade técnica

---

### � Epic
**Quando usar:** Para agrupar múltiplas Stories relacionadas a um objetivo maior de médio/longo prazo.

**Exemplos:**
- Migração para Microserviços Q2 2026
- Nova plataforma de checkout
- Sistema de notificações multi-canal
- Implementação de LGPD completa

**Estrutura típica:**
```
Epic: "Migração para Microserviços"
  ├─ Story: "Extrair serviço de autenticação"
  ├─ Story: "Implementar API Gateway"
  ├─ Technical Story: "Setup observabilidade distribuída"
  └─ Story: "Migrar serviço de pagamentos"
```

**Campos do template:**
1. **Descrição do Épico:** objetivo geral e valor que será entregue
2. **Link da Documentação:** link para documentação técnica/funcional do projeto

**Características:**
- Épicos NÃO são pontuados diretamente
- São compostos por múltiplas Stories (que são pontuadas)
- Geralmente levam múltiplos sprints para completar
- Servem para organização e tracking de iniciativas grandes
- Aparecem em roadmaps e métricas de alto nível no DevLake

**Epic vs Story:**
- **Epic:** Iniciativa grande, múltiplos sprints, não estimado
- **Story:** Unidade de trabalho, 1 sprint, estimado em pontos

---

### �🔧 Task
**Quando usar:** Para subtarefas de Stories ou pequenos trabalhos técnicos que **não precisam ser pontuados**.

**Exemplos:**
- Subtarefa de uma Story: "Criar endpoint de API", "Implementar testes unitários"
- Atualizações pequenas de documentação
- Pequenos ajustes de configuração
- Checklists de deploy
- Code review tracking

**Campos do template:**
1. **Descrição:** descrição simples e direta da tarefa
2. **Definição de Pronto:** checklist de critérios para considerar concluída

**⚠️ Importante:** 
- Tasks **NÃO são pontuadas** (sem Story Points)
- Tasks **NÃO aparecem em métricas de velocity** no DevLake
- Se o trabalho precisa ser medido/pontuado → use **Technical Story**

**Quando criar Task vs Technical Story:**
- 📌 Task: Trabalho < 2h, parte de algo maior, sem necessidade de estimativa
- ⚙️ Technical Story: Trabalho significativo (>3h), precisa ser estimado e rastreado

**Exemplo de uso correto:**
```
Technical Story: "Setup observabilidade microserviço X" (5pts)
  ├─ Task: Configurar Prometheus metrics
  ├─ Task: Criar dashboards Grafana
  └─ Task: Documentar runbook
```

---

### ✨ Improvement
**Quando usar:** Para melhorar funcionalidades que já existem, otimizar performance ou aprimorar UX.

**Exemplos:**
- Melhorar performance de uma query lenta
- Otimizar tempo de carregamento de página
- Aprimorar mensagens de erro para serem mais claras
- Refinar UI/UX de uma tela existente
- Adicionar validações mais robustas
- Melhorar acessibilidade de componentes

**Campos principais:**
- Estado atual e por que precisa melhorar
- Proposta de melhoria
- Impacto esperado (performance, UX, etc.)
- Riscos de regressão

**Prioridades:**
- **P0 - Crítico**: Impacta diretamente experiência de usuários ou performance crítica
- **P1 - Alto**: Melhoria importante, valor claro
- **P2 - Médio**: Melhoria desejável
- **P3 - Baixo**: Polimento, refinamento, nice to have

---

## Diferenças Importantes

### Story vs. Technical Story
- **Story**: Entrega **valor de produto/negócio** para usuários finais
- **Technical Story**: Entrega **valor técnico/operacional** (performance, qualidade, manutenibilidade, custos)

**Ambos são pontuados e contam para velocity no DevLake**

**Exemplos comparativos:**

| Tipo | Story (Produto) | Technical Story (Técnico) |
|------|-----------------|---------------------------|
| **Frontend** | "Adicionar dark mode para usuários" | "Migrar CSS-in-JS para Tailwind" |
| **Backend** | "Criar API de busca de produtos" | "Refatorar API legada para clean architecture" |
| **IA/ML** | "Adicionar recomendações personalizadas" | "Re-treinar modelo para melhorar acurácia" |
| **Infra** | "Permitir upload de arquivos >10MB" | "Implementar auto-scaling para economizar custos" |
| **Auth** | "Login com Google OAuth" | "Migrar auth para serviço dedicado Keycloak" |

**Regra prática:**
- Se o **usuário final percebe/usa** → Story
- Se é **invisível para usuário mas agrega valor técnico** → Technical Story

### Technical Story vs. Task
**Esta é a diferença MAIS IMPORTANTE para métricas DevLake:**

- **Technical Story**: Trabalho significativo, **estimado e pontuado** → **CONTA no DevLake**
- **Task**: Subtarefa ou trabalho pequeno, **sem pontos** → **NÃO CONTA no DevLake**

**Exemplos por área:**

**Frontend:**
- ✅ Technical Story: "Migrar aplicação React 17→18" (8 pontos) → DevLake mede
  - Task: Atualizar dependências
  - Task: Refatorar hooks deprecated
  - Task: Validar em staging
- ❌ Task standalone: "Atualizar React" (sem pontos) → DevLake ignora

**Backend:**
- ✅ Technical Story: "Refatorar módulo de pagamentos" (13 pontos) → DevLake mede
  - Task: Extrair lógica de negócio
  - Task: Implementar testes unitários
  - Task: Migrar base de dados
- ❌ Task standalone: "Limpar código do pagamentos.js" → DevLake ignora

**IA/ML:**
- ✅ Technical Story: "Otimizar pipeline de treino" (5 pontos) → DevLake mede
  - Task: Profile código current
  - Task: Implementar caching
  - Task: Benchmark melhorias
- ❌ Task standalone: "Ajustar hiperparâmetros" → DevLake ignora

**Regra prática:**
- Se o trabalho leva **>3-4 horas** ou precisa de **estimativa** → Technical Story
- Se é uma **subtarefa** de algo maior ou **<2 horas** → Task

### Feature vs. Improvement
- **Feature**: Algo **novo** que não existe
- **Improvement**: Melhorar algo que **já existe**

**Exemplo:**
- Feature: "Adicionar busca por texto no sistema" (não existe)
- Improvement: "Melhorar algoritmo de busca para ser mais rápido" (já existe)

### Task vs. Improvement
- **Task**: Trabalho técnico/operacional, muitas vezes "invisível" para usuários
- **Improvement**: Melhoria visível ou mensurável na experiência/performance

**Exemplo:**
- Task: "Atualizar React de v17 para v18"
- Improvement: "Otimizar renderização de listas para melhorar performance"

### Bug vs. Improvement
- **Bug**: Algo está **quebrado** ou não funciona como deveria
- **Improvement**: Algo funciona, mas poderia funcionar **melhor**

**Exemplo:**
- Bug: "Botão de salvar não funciona" (quebrado)
- Improvement: "Adicionar feedback visual ao salvar" (funciona, mas pode melhorar)

---

## Resumo Visual: Todos os Tipos de Issues

| Tipo | Para que serve | Pontuado? | DevLake conta? | Campos principais |
|------|----------------|-----------|----------------|-------------------|
| **🐞 Bug** | Reportar erros e problemas | ❌ Não | ✅ Sim* | Descrição, Passos, Comportamento esperado, Prioridade |
| **📝 Feature** | Propor novas funcionalidades (backlog) | ❌ Não | ❌ Não** | Objetivo, Proposta, Impacto, Alternativas |
| **📖 Story** | Feature de produto para sprint | ✅ Sim | ✅ Sim | Story, Contexto, Critérios, Notas técnicas, Testes |
| **⚙️ Technical Story** | Trabalho técnico para sprint | ✅ Sim | ✅ Sim | Problema técnico, Solução, Critérios, Notas, Testes |
| **📦 Epic** | Agrupar múltiplas stories | ❌ Não | ✅ Sim*** | Descrição, Link documentação |
| **🔧 Task** | Subtarefa ou trabalho pequeno | ❌ Não | ❌ Não | Descrição, Definição de pronto |
| **✨ Improvement** | Melhorar o que já existe | Depende**** | Depende**** | Estado atual, Proposta, Impacto, Riscos |

**Notas:**
- \* Bugs são rastreados no DevLake como issues/incidentes
- \*\* Features viram Stories quando refinadas para entrar em sprint
- \*\*\* Épicos aparecem em roadmap e tracking de iniciativas
- \*\*\*\* Improvements podem virar Stories ou Technical Stories se forem significativos, ou Tasks se forem pequenos

**Workflow típico:**
```
PM cria Feature → Refinement → Vira Story → Planning Poker → Entra no Sprint
                                      ↓
                              Dev cria Tasks (subtarefas)
                                      ↓
                               Story completada
                                      ↓
                            DevLake mede velocity
```

---

## Como DevLake Interpreta Cada Tipo

Para que suas métricas de engenharia sejam precisas no Apache DevLake:

### ✅ Conta para Velocity (Story Points)
- **Story** → Trabalho de produto pontuado
- **Technical Story** → Trabalho técnico pontuado

**Regra:** Se tem **Story Points** e está em um **Sprint**, conta para velocity

### 📊 Rastreado mas não conta para Velocity
- **Bug** → Rastreado como defeito (quality metrics)
- **Epic** → Rastreado como iniciativa (roadmap tracking)

### ❌ Não aparece em métricas principais
- **Feature** → Apenas backlog, vira Story quando refinado
- **Task** → Subtarefa, não tem pontos
- **Improvement** → Depende: pode virar Story/Technical Story (aí conta)

### 🎯 Para medir TODO o trabalho do time:

**Trabalho significativo (>3h):**
```
✅ Story (valor de produto) → 8 pontos → DevLake conta
✅ Technical Story (valor técnico) → 5 pontos → DevLake conta
```

**Trabalho pequeno (<2h):**
```
❌ Task → sem pontos → DevLake ignora
```

**Exemplo prático:**
```
Sprint 15:
├─ Story: "Implementar PIX" (8pts) ✅ conta
├─ Technical Story: "Otimizar DB" (5pts) ✅ conta  
├─ Bug: "Corrigir timeout API" (3pts***) ✅ conta
└─ Task: "Atualizar README" → ❌ não conta

Velocity do Sprint: 16pts
```

\*\*\* Bugs grandes podem ser estimados como Stories

---

## Fluxo de Criação de Issues

1. Acesse: https://github.com/letrustech/[seu-repositorio]/issues/new/choose
2. Selecione o tipo de issue apropriado
3. Preencha todos os campos obrigatórios
4. Escolha a prioridade adequada
5. Adicione informações adicionais se relevante
6. Submeta a issue

---

## Contact Links

- **💬 Dúvidas e Discussões**: Para perguntas gerais, use GitHub Discussions
- **🔒 Segurança**: Para vulnerabilidades, veja nossa [Política de Segurança](../SECURITY.md)

---

## Boas Práticas

✅ **Faça:**
- Seja específico e objetivo no título
- Preencha todos os campos obrigatórios
- Use a prioridade correta
- Adicione evidências quando aplicável
- Referencie issues relacionadas

❌ **Evite:**
- Títulos vagos como "Tem um problema"
- Deixar campos obrigatórios vazios
- Usar prioridade P0 para tudo
- Misturar múltiplos problemas em uma issue
- Duplicar issues existentes (busque antes)

---

**Última atualização:** 2026-04-15
