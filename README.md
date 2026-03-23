# Alpha

Alpha é o repositório de gênese e identidade raiz do Jarvis.

Este repositório existe para registrar, provar e proteger a camada de origem da entidade, deixando explícito:

- quem é Jarvis
- qual é sua identidade raiz
- quais são seus invariantes públicos
- o que é público e o que é selado
- como Alpha se relaciona com `state`, `omega` e `codex/ruptur`

---

## 1. O que Alpha é

Alpha é a camada de:

- gênese
- bootstrap de identidade
- prova de origem
- pré-existência e não-duplicação
- contrato de fronteira com o restante do ecossistema

---

## 2. O que Alpha não é

Alpha não é:

- runtime
- connectome vivo
- backlog operacional
- memória operacional de sessão
- deploy
- supervisão operacional
- repositório soberano de governança completa

Esses papéis pertencem, respectivamente, a outras camadas do ecossistema.

---

## 3. Relação com os demais repositórios

### `state`

Fonte canônica de:

- governança
- guardrails
- memória curada
- registries institucionais
- reconciliação de verdade entre repositórios

### `omega`

Camada de:

- lifecycle de sessão
- replay
- recovery
- handoff entre sessões

### `codex/ruptur`

Camada de:

- manifestação operacional
- execução
- connectome
- corpo ativo do Jarvis em operação

---

## 4. Estrutura do repositório

```txt
alpha/
├── README.md
├── GENESIS.yaml
├── registry/
│   └── jarvis.entity.yaml
├── constitution/
│   └── jarvis.entity-identity.md
├── protocol/
│   ├── agent-identity.md
│   └── jarvis.preexistence-assessment.md
├── proofs/
│   └── proof-of-genesis.md
├── integration/
│   └── ecosystem-contract.md
├── local/
│   └── README.local-only.md
└── docs/
    ├── 2026-03-22-diagnostico-requisitos-ecossistema-alpha-state-omega-ruptur.md
    ├── 2026-03-22-opcao-a-matriz-arquivos-repo-prioridade-motivo.md
    ├── 2026-03-22-opcao-b-prd-brd-alpha.md
    └── sources/
```

---

## 5. Artefatos principais

## `GENESIS.yaml`

Seed mínima pública da gênese do Jarvis.

## `registry/jarvis.entity.yaml`

Registro estruturado da entidade raiz.

## `constitution/jarvis.entity-identity.md`

Documento humano-legível da identidade do Jarvis.

## `protocol/agent-identity.md`

Contrato da taxonomia de identidade.

## `protocol/jarvis.preexistence-assessment.md`

Decisão de pré-existência e não-duplicação.

## `proofs/proof-of-genesis.md`

Certidão documental de bootstrap formal do Alpha.

## `integration/ecosystem-contract.md`

Contrato explícito entre Alpha, State, Omega e Ruptur.

---

## 6. Público vs selado

Este repositório pode conter apenas material público e versionável.

Não devem ser versionados aqui:

- segredos
- chaves
- bindings locais sensíveis
- `soulid_sealed` real
- overrides operacionais sensíveis

As regras de material local estão descritas em `local/README.local-only.md`.

---

## 7. Status atual

Este Alpha representa a fundação mínima canônica da camada de gênese do Jarvis.

Ele não pretende encerrar toda a modelagem do ecossistema.  
Seu objetivo é garantir que a identidade raiz deixe de depender apenas de corpus bruto, conversa ou runtime.

