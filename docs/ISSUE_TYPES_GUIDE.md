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

**Campos principais:**
- Passos para reproduzir o problema
- Resultado esperado vs. resultado atual
- Ambiente (SO, navegador, versão)
- Evidências (screenshots, logs)

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

### 🔧 Task
**Quando usar:** Para tarefas técnicas, manutenções, refatorações ou trabalho operacional.

**Exemplos:**
- Atualizar dependências do projeto
- Refatorar código legado
- Configurar pipeline de CI/CD
- Migrar banco de dados
- Atualizar documentação técnica
- Setup de ambiente de desenvolvimento

**Campos principais:**
- Checklist detalhado de tarefas
- Dependências e bloqueios
- Notas técnicas e comandos úteis
- Definição de pronto

**Prioridades:**
- **P0 - Crítico**: Urgente, bloqueando outros trabalhos
- **P1 - Alto**: Importante para o sprint/release atual
- **P2 - Médio**: Pode ser feito no próximo sprint
- **P3 - Baixo**: Backlog, sem urgência definida

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

**Última atualização:** 2026-02-02
