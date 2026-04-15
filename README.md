# letrustech/.github

Repositório utilizado para centralizar os templates de pull requests, issues e políticas dos projetos da organização letrustech.

## 📋 Issue Templates Padronizados

Este repositório define os tipos de issues padrão para toda a organização.

### Tipos Disponíveis

| Tipo | Quando Usar | Pontuado? | DevLake |
|------|-------------|-----------|---------|
| 🐞 **Bug** | Reportar erros ou comportamentos inesperados | ❌ | ✅ Rastreado |
| 📝 **Feature** | Propor novas funcionalidades (backlog) | ❌ | ❌ |
| 📖 **Story** | Feature de produto para sprint (estimado) | ✅ | ✅ Velocity |
| ⚙️ **Technical Story** | Trabalho técnico para sprint (estimado) | ✅ | ✅ Velocity |
| 📦 **Epic** | Agrupar múltiplas stories em uma iniciativa | ❌ | ✅ Roadmap |
| 🔧 **Task** | Subtarefa ou trabalho pequeno sem pontos | ❌ | ❌ |
| ✨ **Improvement** | Melhorar funcionalidades existentes | Depende | Depende |

### Templates Configurados

```
.github/ISSUE_TEMPLATE/
├── bug.yaml              # 🐞 Bugs e erros
├── story.yaml            # 📖 Stories de produto
├── technical-story.yaml  # ⚙️ Stories técnicas
├── epic.yaml             # 📦 Épicos
└── task.yaml             # 🔧 Tasks
```

### Como Usar

Ao criar uma nova issue em qualquer repositório da organização:

1. Clique em "New Issue"
2. Escolha o template apropriado:
   - **Story** ou **Technical Story** → trabalho que entra em sprint (pontuado)
   - **Task** → subtarefa ou trabalho pequeno (não pontuado)
   - **Bug** → erros e problemas
   - **Epic** → agrupar múltiplas stories
3. Preencha todos os campos obrigatórios
4. Para Bugs: selecione a prioridade (P0-P3)
5. Para Stories: será estimado em Planning Poker
6. Submeta a issue

**Workflows típicos:**

**Feature de produto:**
```
PM cria Feature → Refinement → Vira Story → Planning Poker → Sprint
```

**Trabalho técnico:**
```
Lead/Dev cria Technical Story → Planning Poker → Sprint
```

**Trabalho urgente:**
```
Criar Story ou Technical Story (mesmo sem Epic) → Pontuar → Sprint
```

Para mais detalhes, consulte o [Guia Completo de Issue Types](docs/ISSUE_TYPES_GUIDE.md).

## 📝 Pull Request Template

Template padronizado para Pull Requests disponível em `.github/PULL_REQUEST_TEMPLATE.md`.

## 🔒 Segurança

Para reportar vulnerabilidades de segurança, consulte nossa [Política de Segurança](SECURITY.md).

## 📚 Recursos

- **[Guia Completo de Issue Types](docs/ISSUE_TYPES_GUIDE.md)**: Documentação detalhada sobre todos os tipos
- **Dúvidas e Discussões**: Use [GitHub Discussions](https://github.com/orgs/letrustech/discussions)
- **Templates**: `.github/ISSUE_TEMPLATE/`
- **Política de Segurança**: `SECURITY.md`

## 📊 Integração com DevLake

Os templates estão otimizados para Apache DevLake:

- ✅ **Stories** e **Technical Stories** → contam para **velocity** (quando pontuados e em sprint)
- ✅ **Bugs** → rastreados como **defeitos** (quality metrics)
- ✅ **Épicos** → rastreados como **iniciativas** (roadmap)
- ❌ **Tasks** → subtarefas internas (não contam para velocity)

**Regra de ouro:** Se o trabalho precisa ser medido → use **Story** ou **Technical Story** (pontuado)

---

**Última atualização:** 2026-04-15
