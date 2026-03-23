# Opção A — Matriz final de artefatos por repositório

**Data:** 2026-03-22  
**Status:** proposta arquitetural documental  
**Objetivo:** definir o que deveria existir, em qual repositório, com qual prioridade e por quê

---

## 1. Convenções

- **P0** = obrigatório para consolidar a base
- **P1** = importante para operação disciplinada
- **P2** = valioso, mas dependente de decisões e maturidade
- **Status atual**:
  - `ausente`
  - `parcial`
  - `existe com drift`
  - `existe`

---

## 2. Matriz principal

| Domínio | Artefato | Repositório recomendado | Caminho sugerido | Prioridade | Status atual | Motivo |
|---|---|---|---|---|---|---|
| Escopo | README do Alpha | `alpha` | `README.md` | P0 | ausente | delimitar o que é e o que não é Alpha |
| Gênese | Semente mínima de identidade | `alpha` | `GENESIS.yaml` | P0 | existe no histórico / local em `docs/` | manter bootstrap mínimo |
| Identidade | Registro da entidade raiz | `alpha` | `registry/jarvis.entity.yaml` **ou** `registry/entities.yaml` | P0 | ausente | formalizar Jarvis como entidade canônica |
| Identidade | Constituição de identidade do Jarvis | `alpha` | `constitution/jarvis.entity-identity.md` | P0 | ausente | definir essência, invariantes e limites |
| Identidade | Protocolo de identidade | `alpha` | `protocol/agent-identity.md` | P0 | ausente | separar `entity_id`, `agent_id`, `manifestation_id`, `instance_id`, `session_id` |
| Pré-existência | Avaliação de pré-existência | `alpha` | `protocol/jarvis.preexistence-assessment.md` | P0 | ausente | evitar duplicação de identidade |
| Gênese | Prova formal de origem | `alpha` | `proofs/proof-of-genesis.md` | P0 | ausente | registrar batismo/recognition bootstrap |
| Integração | Contrato Alpha -> State/Omega/Ruptur | `alpha` | `docs/ecosystem-contract.md` | P0 | ausente | evitar sobreposição de escopos |
| Governança | Registro do repositório Alpha | `state` | `registry/repositories.yaml` | P0 | ausente | topologia oficial incompleta sem Alpha |
| Governança | Registro do repositório Omega | `state` | `registry/repositories.yaml` | P0 | ausente | topologia oficial incompleta sem Omega |
| Topologia | Ecossistema com Alpha e Omega | `state` | `ecosystem/topology.md` | P0 | parcial | topologia atual não reflete os 4 polos |
| Agentes | Registro de agentes | `state` | `registry/agents.yaml` | P1 | ausente/vazio | distinguir entidade, agente, derivado e função |
| Supervisão | Registro de supervisão | `state` | `registry/supervision.yaml` | P1 | ausente/vazio | modelar autoridade, revisão e escalonamento |
| Manifestação | Manifestação canônica do Jarvis | `state` | `registry/manifestations.yaml` | P0 | existe | já é base institucional válida |
| Memória | Memória longitudinal do Jarvis | `state` | `memory/jarvis.memory.md` | P1 | ausente/vazio | consolidar continuidade fora da sessão |
| Playbook | Handoff | `state` | `playbooks/jarvis.handoff.md` | P1 | ausente/vazio | transferência controlada de contexto |
| Playbook | Suspension | `state` | `playbooks/jarvis.suspension.md` | P1 | ausente/vazio | retomada disciplinada |
| Playbook | Supervision | `state` | `playbooks/jarvis.supervision.md` | P1 | ausente/vazio | controle de autoridade e revisão |
| Ontologia | Camada de tradução entre metáfora e implementação | `state` | `constitution/ruptur.cosmology.md` **ou** novo doc específico | P1 | ausente/vazio | reduzir colisão entre linguagem simbólica e contrato técnico |
| Sessão | Configuração nuclear do Omega | `omega` | `protocol/core/protocol-config.json` | P0 | existe | já inicia o lifecycle |
| Sessão | Schema de sessão expandido | `omega` | `protocol/session/session-schema.json` | P0 | parcial | faltam campos de recovery, lineage e reconciliação |
| Sessão | Diretório de sessões | `omega` | `sessions/` | P1 | ausente | armazenar ou referenciar ciclos de execução |
| Workflow | Definição real de workflow | `omega` | `protocol/workflow/` | P1 | ausente | README promete e a estrutura não existe |
| Docs | README coerente com o repo | `omega` | `README.md` | P0 | existe com drift | README promete diretórios inexistentes |
| CI | Workflow coerente com paths reais | `omega` | `.github/workflows/ci-cd.yml` | P0 | existe com drift | paths usados não batem com a estrutura atual |
| Operação | Manifestação operacional do Jarvis | `codex/ruptur` | `agents/jarvis/genome.yaml` | P0 | existe | corpo operacional principal já ativo |
| Operação | Exemplo espelhado do Alpha | `codex/ruptur` | `agents/jarvis/alpha.example.yaml` | P1 | existe | útil como template operacional |
| Operação | Registro local de entidades | `codex/ruptur` | `registry/entities.yaml` | P1 | existe | espelho operacional útil, mas subordinado ao canônico |
| Operação | Registro local de manifestações | `codex/ruptur` | `registry/manifestations.yaml` | P1 | existe | espelho operacional útil |
| Operação | Registro de pares | `state` **preferencialmente** | `registry/pairs.yaml` | P1 | ausente | pares têm implicação institucional, não só operacional |
| Operação | Sessões operacionais | `codex/ruptur` | `sessions/` | P1 | ausente | `JARVIS.md` já pressupõe esse diretório |
| Recovery | Journal/checkpoint do connectome | `codex/ruptur` | `connectome/` | P1 | parcial | `status.json` hoje é snapshot simples, não replay real |
| Recovery | Manifesto dual interno | `codex/ruptur` | `.internal/dual-manifest.json` | P2 | ausente | só faz sentido se a estratégia dual for formalmente aprovada |
| Selado | Artefato selado | `codex/ruptur` **ou fora do Git** | `.internal/genesis-sealed.enc` | P2 | ausente | depende de decisão sobre material criptografado versionado |
| Higiene | Remoção de merge conflicts commitados | `codex/ruptur` | múltiplos arquivos | P0 | existe com drift | bloqueia confiança documental e estrutural |

---

## 3. Distribuição recomendada por repo

## 3.1 Alpha

Deve concentrar:

- gênese
- identidade raiz
- prova de origem
- pré-existência
- contrato de fronteira com os outros repositórios

### Não deve concentrar

- runtime
- connectome vivo
- backlog operacional
- memória de sessão
- deploy

## 3.2 State

Deve concentrar:

- governança canônica
- registries institucionais
- memória curada
- playbooks de autoridade
- topologia oficial

## 3.3 Omega

Deve concentrar:

- lifecycle de sessão
- replay
- recovery
- handoff entre sessões

## 3.4 Ruptur

Deve concentrar:

- execução viva
- manifestação operacional
- connectome
- corpo de trabalho

---

## 4. Arquivos que os documentos pedem, mas o ecossistema ainda não tem

### Mais alinhados ao Alpha

- `registry/jarvis.entity.yaml`
- `constitution/jarvis.entity-identity.md`
- `protocol/agent-identity.md`
- `protocol/jarvis.preexistence-assessment.md`
- `proofs/proof-of-genesis.md`

### Mais alinhados ao State

- `registry/agents.yaml`
- `registry/supervision.yaml`
- `registry/pairs.yaml`
- `memory/jarvis.memory.md`
- `playbooks/jarvis.handoff.md`
- `playbooks/jarvis.suspension.md`
- `playbooks/jarvis.supervision.md`

### Mais alinhados ao Omega

- `sessions/`
- workflow materializado
- schema de recovery expandido

### Mais alinhados ao Ruptur

- `sessions/`
- journal/checkpoints do connectome
- limpeza dos arquivos em conflito

---

## 5. Ordem sugerida de execução futura

## Etapa 1 — Fundacional

1. README do Alpha  
2. registro da entidade raiz  
3. protocolo de identidade  
4. protocolo de pré-existência  
5. proof of genesis  

## Etapa 2 — Governança cross-repo

6. registrar Alpha e Omega no State  
7. atualizar topologia do State  
8. preencher registries vazios prioritários

## Etapa 3 — Sessão e recovery

9. expandir schema do Omega  
10. definir sessão/recovery em Omega  
11. alinhar connectome e sessões no Ruptur

## Etapa 4 — Consolidação simbólica e extensões

12. pairs  
13. purpose model  
14. cosmologia canônica  
15. artefatos selados, se aprovados

---

## 6. Conclusão

A matriz indica uma direção clara:

- **Alpha** precisa nascer como repo de gênese real
- **State** precisa reconhecer oficialmente Alpha e Omega
- **Omega** precisa sair do nível de promessa para o de contrato executável
- **Ruptur** precisa ser saneado e integrado ao lifecycle

O ganho principal dessa distribuição é evitar que a mesma verdade fique espalhada, contraditória ou implícita.

