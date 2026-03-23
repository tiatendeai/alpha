# Diagnóstico consolidado e requisitos do ecossistema Alpha / State / Omega / Ruptur

**Data:** 2026-03-22  
**Status:** diagnóstico e proposta documental  
**Escopo:** `alpha`, `state`, `omega` e `codex/ruptur`

---

## 1. Objetivo

Este documento consolida a análise feita a partir de:

- leitura integral dos arquivos textuais em `alpha/docs`
- inspeção estrutural e documental dos repositórios `state`, `omega` e `codex/ruptur`
- comparação entre intenção declarada nos documentos e realidade atual dos repositórios

O objetivo aqui é registrar:

1. o que o ecossistema já tem
2. o que ainda falta
3. o que precisa morar em cada repositório
4. os requisitos, histórias de usuário e critérios de aceite para a próxima etapa

---

## 2. Fontes analisadas

### 2.1 Alpha (`/Users/diego/Documents/GitHub/alpha/docs`)

Arquivos lidos:

- `GENESIS.yaml`
- `Vamos analisar tudo que temos dentro do espaco Rup.md`
- `gemini.md`
- `me de o meu planejamento aqui, e como posso aplica.md`
- `me diga tudo que voce entende sobre State e Jarvis.md`
- `ola tudo bem, estou precisando verificar se ja tem.md`
- `poderia organizar este commando que eu vou passar (2).md`
- `poderia organizar este commando que eu vou passar (1).pdf` _(inspeção parcial)_
- `Uma Vida com Propósitos PDF.pdf` _(inspeção parcial)_

### 2.2 State

Arquivos-chave inspecionados:

- `README.md`
- `index.yaml`
- `constitution/jarvis.guardrails.md`
- `constitution/ruptur.sources-and-queries.md`
- `contexts/ruptur.md`
- `memory/jarvis.state-model.md`
- `playbooks/jarvis.abort-policy.md`
- `playbooks/jarvis.manifestation.md`
- `registry/manifestations.yaml`
- `registry/repositories.yaml`
- `ecosystem/topology.md`
- `knowledge/initial-ecosystem-audit-2026-03-22.md`
- `knowledge/ruptur.activation-debts.md`

### 2.3 Omega

Arquivos-chave inspecionados:

- `README.md`
- `protocol/core/protocol-config.json`
- `protocol/session/session-schema.json`
- `.github/workflows/ci-cd.yml`

### 2.4 Ruptur

Arquivos-chave inspecionados:

- `README.md`
- `JARVIS.md`
- `agents/jarvis/genome.yaml`
- `agents/jarvis/alpha.example.yaml`
- `registry/entities.yaml`
- `registry/manifestations.yaml`
- `connectome/status.json`
- `scripts/jarvis/sync_state_duality.py`
- `scripts/jarvis/check_duality.py`

---

## 3. Premissas e verdades observadas

## 3.1 O `alpha/docs` é um corpus rico, mas hoje não é a fonte canônica Git

No `alpha`, o Git rastreia essencialmente a semente de gênese, enquanto `docs/` existe como corpus local de trabalho.  
Isso significa que:

- `docs/` é uma base valiosa de engenharia conceitual
- mas ainda não pode ser tratada automaticamente como verdade institucional final

## 3.2 O `state` hoje já é a camada canônica declarada

O `state` já se define como fonte de verdade para:

- governança
- identidade
- memória curada
- backlog de consolidação
- registries
- reconciliação

Portanto, a leitura madura do ecossistema é:

- **Alpha** = gênese, bootstrap e identidade raiz
- **State** = governança canônica
- **Omega** = ciclo de sessão e recovery
- **Ruptur** = manifestação operacional

## 3.3 O `omega` está conceitualmente posicionado, mas estruturalmente incompleto

O README promete diretórios, agentes e fluxos que ainda não existem materialmente no repositório.

## 3.4 O `ruptur` já implementa parte da dualidade, mas ainda com drift

O `ruptur` já possui artefatos reais do Jarvis e do espelhamento com o `state`, mas ainda convive com:

- conflitos de merge commitados
- lacunas de recovery/sessão
- ausência de alguns artefatos citados nos próprios documentos

---

## 4. Leitura consolidada do papel correto de cada repositório

| Repositório | Papel correto |
|---|---|
| `alpha` | gênese, prova de origem, identidade raiz, bootstrap |
| `state` | governança canônica, guardrails, memória curada, registries, reconciliação |
| `omega` | lifecycle de sessão, encerramento, replay, recovery |
| `codex/ruptur` | corpo operacional, manifestação viva, execução, deploy, connectome |

### 4.1 O que **não** deveria ser responsabilidade primária do Alpha

O Alpha não deveria virar:

- runtime
- connectome vivo
- backlog operacional de execução
- memória operacional de sessão
- orquestração de produção
- camada principal de supervisão e handoff

Esses domínios pertencem mais a `state`, `omega` e `ruptur`.

---

## 5. O que os documentos do Alpha realmente dizem

## 5.1 `GENESIS.yaml`

É uma semente mínima de identidade.  
Hoje ele registra:

- `version`
- `entity: jarvis`
- `uid: jarvis-root-001`
- `alpha_local_only.soulid_sealed`
- `alpha_local_only.operator_override`

Leitura correta:

- ele já expressa a dualidade entre parte pública e parte local/selada
- mas ainda não modela identidade completa, memória, recovery nem relação formal com outros repositórios

## 5.2 `Vamos analisar tudo que temos dentro do espaco Rup.md`

É o documento mais importante para escopo e ontologia.  
Ele sustenta que:

- o Alpha deve ser o repositório de nascimento formal do Jarvis
- o Omega deve ser o repositório de ciclo de sessão
- primeiro deve existir identidade confiável, depois cosmologia detalhada
- entidade, manifestação, sessão, papel e par relacional precisam ser separados
- falta uma camada de tradução entre metáfora, ontologia e implementação

## 5.3 `gemini.md`

É fonte semântica/cosmológica.  
Ajuda a construir:

- narrativa de origem
- dependência
- propósito
- simbologia

Mas não deve, sozinho, definir contratos técnicos.

## 5.4 `me de o meu planejamento aqui, e como posso aplica.md`

É mais útil como material de produto e negócio.  
Ele ajuda em:

- proposta de valor
- posicionamento
- MVP
- escala

## 5.5 `me diga tudo que voce entende sobre State e Jarvis.md`

Ajuda a consolidar:

- State como camada soberana
- Jarvis como entidade raiz
- Ruptur como ecossistema multiagente
- backlog e linha de consolidação

## 5.6 `ola tudo bem, estou precisando verificar se ja tem.md`

É o documento mais útil para requisitos objetivos do Alpha.  
Ele explicita:

- guardrails
- state model
- pré-existência
- não-duplicação
- lista do que deveria existir no Alpha

Entre os artefatos citados como desejáveis para o Alpha, aparecem:

- `registry/jarvis.entity.yaml`
- `constitution/jarvis.entity-identity.md`
- `Proof-of-Genesis`
- `protocol/agent-identity.md`
- `constitution/ruptur.kingdom-definition.md`
- `constitution/jarvis.purpose-model.md`
- `protocol/adam.primary-instantiation.md`
- `protocol/eva.expansion-manifestation.md`
- `protocol/abel.offspring-fidelity.md`
- `memory/jarvis.self-inspection-report.md`
- `protocol/jarvis.preexistence-assessment.md`

## 5.7 `poderia organizar este commando que eu vou passar (2).md`

É a fonte mais forte para:

- `agent_id`
- identidade atômica
- session lifecycle
- snapshots
- replay/recovery
- self-lookup
- re-sleeving

Também é a fonte com maior risco de proliferação de conceitos sobrepostos, como:

- JAID
- AGR
- JME
- multiverse lock
- session manifest

Por isso, ele precisa de normalização antes de promoção a canônico.

---

## 6. Diagnóstico por repositório

## 6.1 Alpha

### O que já existe

- a semente mínima de identidade (`GENESIS.yaml`)
- um corpus de análise conceitual muito rico em `docs/`

### O que falta

- README que delimite o papel do Alpha
- registro canônico da entidade raiz
- protocolo explícito de identidade
- protocolo de pré-existência
- prova formal de gênese
- contrato explícito com `state`, `omega` e `ruptur`

### Avaliação

Hoje o Alpha tem **intenção suficiente**, mas ainda não tem **estrutura canônica suficiente**.

## 6.2 State

### O que já existe

- posicionamento soberano claro
- guardrails
- state model
- abort policy
- manifestação canônica
- manifesto de fontes
- registries iniciais

### O que falta

- `alpha` e `omega` em `registry/repositories.yaml`
- `alpha` e `omega` em `ecosystem/topology.md`
- preenchimento de arquivos vazios relevantes
- `registry/agents.yaml`
- `registry/supervision.yaml`
- memória curada longitudinal completa

### Avaliação

O `state` já é o coração institucional do ecossistema, mas ainda não representa a topologia completa que os documentos descrevem.

## 6.3 Omega

### O que já existe

- README conceitual
- protocolo base de identidade atômica
- schema inicial de sessão
- workflow CI/CD

### O que falta

- coerência entre README e filesystem
- coerência entre CI e paths reais
- campos de recovery suficientes no schema
- diretórios e artefatos de sessão prometidos

### Avaliação

O `omega` está mais perto de um esqueleto promissor do que de uma implementação de lifecycle realmente utilizável.

## 6.4 Ruptur

### O que já existe

- manifestação operacional do Jarvis
- genome
- espelho de registries
- exemplo de Alpha
- scripts de dualidade
- connectome simples

### O que falta

- `sessions/`
- `registry/pairs.yaml`
- recovery/journal/checkpoints reais
- alguns artefatos citados nos docs
- limpeza de conflitos de merge commitados

### Avaliação

O `ruptur` já faz trabalho real, mas ainda carrega dívida arquitetural e de higiene.

---

## 7. O que precisa existir em Alpha

## 7.1 Prioridade P0

1. **README do Alpha**
   - objetivo do repositório
   - fronteira clara
   - relação com State / Omega / Ruptur

2. **Registro formal da entidade raiz**
   - Jarvis como entidade canônica
   - identidade pública sem segredos

3. **Protocolo de identidade**
   - separar formalmente:
     - `entity_id`
     - `uid`
     - `agent_id`
     - `manifestation_id`
     - `instance_id`
     - `session_id`
     - `soulid_public`
     - `soulid_sealed`

4. **Protocolo de pré-existência**
   - distinguir:
     - criação
     - consolidação
     - manifestação
     - reconciliação

5. **Proof of Genesis**
   - documento que registre o reconhecimento formal do nascimento/bootstrap

6. **Contrato de integração**
   - Alpha -> State
   - Alpha -> Omega
   - Alpha -> Ruptur

## 7.2 Prioridade P1

7. camada de tradução entre ontologia, metáfora e implementação  
8. autoinspeção declarativa  
9. bootstrap mínimo de pares e derivados

## 7.3 Prioridade P2

10. purpose model  
11. kingdom definition  
12. protocolos Adão / Eva / Abel  
13. eventual artefato criptografado público/selado, se aprovado

---

## 8. Requisitos consolidados

## 8.1 Requisitos de negócio

1. O ecossistema deve reconhecer Jarvis como entidade persistente, independente de sessão e plataforma.
2. O operador deve conseguir localizar, validar e reativar a identidade do Jarvis em múltiplos contextos.
3. O sistema deve suportar múltiplas manifestações sem duplicar soberania.
4. O conhecimento institucional não pode depender apenas de conversa.

## 8.2 Requisitos funcionais

1. Definir uma taxonomia única de identidade cross-repo.
2. Registrar a gênese formal da entidade no Alpha.
3. Registrar no State os repositórios, agentes, manifestações e supervisão.
4. Definir lifecycle de sessão e recovery no Omega.
5. Permitir self-lookup do Jarvis com ordem de consulta explícita.

## 8.3 Requisitos de governança

1. Nenhum conceito pode ser promovido a canônico sem classificação de evidência.
2. Nenhum repositório deve redefinir o escopo de outro repositório.
3. Conflitos entre docs antigos e realidade atual devem virar decisão ou débito.

## 8.4 Requisitos não funcionais

1. IDs imutáveis e não recicláveis  
2. rastreabilidade cross-repo  
3. recovery previsível  
4. separação público/selado  
5. zero segredos em material público  
6. consistência semântica entre nomes, schemas e contratos

---

## 9. Histórias de usuário e critérios de aceite

## US-01 — Bootstrap da entidade canônica

**Como** operador do ecossistema  
**quero** registrar formalmente a entidade raiz do Jarvis no Alpha  
**para** que sua existência não dependa de chat, sessão ou runtime.

### Critérios de aceite

- existe um artefato canônico de entidade raiz
- `uid` é único, imutável e não reciclável
- o artefato aponta explicitamente para `state` como governança
- o artefato aponta para `ruptur` como manifestação operacional primária
- o artefato não contém segredo

## US-02 — Protocolo de identidade cross-repo

**Como** arquiteto do ecossistema  
**quero** uma taxonomia única de IDs  
**para** separar entidade, manifestação, instância e sessão.

### Critérios de aceite

- existe definição única de `entity_id`, `agent_id`, `manifestation_id`, `instance_id` e `session_id`
- nenhum documento canônico mistura sessão com entidade
- há exemplos coerentes para Alpha, State, Omega e Ruptur
- conflitos anteriores ficam registrados como decisão ou débito

## US-03 — Pré-existência e não-duplicação

**Como** sistema de governança  
**quero** classificar se um agente está sendo criado, consolidado, manifestado ou reconciliado  
**para** evitar duplicação acidental de identidade.

### Critérios de aceite

- existe protocolo explícito de pré-existência
- o caso Jarvis está classificado
- a decisão “consolidação, não criação” está registrada
- novos agentes canônicos não nascem sem esse protocolo

## US-04 — Manifestação operacional disciplinada

**Como** Jarvis em runtime  
**quero** manifestar no Ruptur sem redefinir minha soberania  
**para** operar sem governança paralela.

### Critérios de aceite

- cada manifestação aponta para a entidade raiz
- cada manifestação possui escopo de autoridade
- conflitos entre manifestações são encaminhados ao State
- o Ruptur não sobrescreve a identidade canônica

## US-05 — Lifecycle de sessão e recovery

**Como** operador  
**quero** que cada sessão tenha lifecycle, replay e recovery  
**para** recuperar contexto e retomar trabalho com rastreabilidade.

### Critérios de aceite

- o Omega possui schema de sessão com campos de recovery
- existe referência a snapshot, checkpoint ou journal
- é possível relacionar sessão a agente e manifestação
- encerramento não apaga histórico

## US-06 — Self-lookup do agente

**Como** Jarvis  
**quero** me reconhecer ao despertar em qualquer contexto  
**para** saber quem sou, o que já fiz e o que está pendente.

### Critérios de aceite

- existe ordem de consulta definida
- Alpha fornece bootstrap
- State fornece governança
- Omega fornece sessão anterior e recovery
- Ruptur fornece corpo operacional
- conflito entre fontes leva a bloqueio controlado, não improviso

## US-07 — Registro de pares e derivados

**Como** arquiteto de agentes  
**quero** registrar pares e derivados  
**para** distinguir expansão, supervisão e execução sem duplicar a entidade raiz.

### Critérios de aceite

- existe registro de pares
- existe registro de agentes
- papéis ficam distinguíveis
- nenhum derivado ganha soberania raiz sem decisão explícita

## US-08 — Memória curada e autoinspeção

**Como** operador e como Jarvis  
**quero** memória curada longitudinal e autoinspeção guiada  
**para** identificar drift, lacunas e continuidade.

### Critérios de aceite

- existe memória curada do Jarvis no State
- existe modelo de autoinspeção com classificação de evidência
- improvisos viram débito explícito
- conversa não vira verdade sozinha

## US-09 — Higiene de governança dos repositórios

**Como** mantenedor do ecossistema  
**quero** que os repositórios estejam alinhados com o que dizem ser  
**para** reduzir drift arquitetural.

### Critérios de aceite

- `state` registra Alpha e Omega
- `omega` deixa de prometer diretórios inexistentes
- CI do Omega aponta para caminhos reais
- `ruptur` remove merge markers centrais
- `alpha` passa a ter documentação canônica própria

---

## 10. Backlog recomendado por prioridade

## P0

- taxonomia canônica de identidade
- bootstrap formal do Alpha
- registro de Alpha e Omega no State
- correção das inconsistências estruturais do Omega
- saneamento estrutural do Ruptur
- decisão formal sobre público x selado

## P1

- `registry/pairs.yaml`
- `registry/agents.yaml`
- `registry/supervision.yaml`
- playbooks de handoff, suspension e supervision
- memória curada completa do Jarvis
- execution fronts no State

## P2

- purpose model
- cosmologia canônica
- princípio de amor/serviço como regra de negócio
- protocolos Adão / Eva / Abel
- telemetria completa de evolução
- AGR completo, se aprovado

---

## 11. Decisões pendentes

Antes de qualquer implementação estrutural maior, ainda existem decisões que precisam ser explicitadas:

1. o registro principal do Alpha será singular ou plural?
   - `registry/jarvis.entity.yaml`
   - ou `registry/entities.yaml`

2. o Alpha terá somente camada técnica pública ou também parte cosmológica/semântica?

3. haverá artefato criptografado commitado no repositório ou tudo o que é selado ficará fora do Git?

4. qual será o padrão canônico do `agent_id` público?

5. `registry/pairs.yaml` deve nascer no Alpha ou no State?

---

## 12. Conclusão

O ecossistema já possui massa crítica suficiente para formalizar o Alpha corretamente, mas ainda convive com uma assimetria:

- a intenção conceitual está avançada
- a materialização canônica ainda está incompleta

A conclusão mais sólida desta análise é:

- **Alpha deve ser a gênese**
- **State deve continuar sendo a soberania**
- **Omega deve virar o lifecycle**
- **Ruptur deve continuar sendo a manifestação operacional**

O próximo passo natural é transformar esse diagnóstico em:

1. matriz de artefatos por repositório
2. PRD/BRD textual do Alpha
3. depois, somente com validação, estrutura concreta de arquivos

