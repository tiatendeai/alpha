# Contrato do ecossistema Alpha / State / Omega / Ruptur

**Status:** contrato de fronteira documental  
**Escopo:** definição de responsabilidades entre repositórios

---

## 1. Objetivo

Este documento existe para impedir sobreposição, ambiguidade e redefinição indevida de escopo entre os repositórios do ecossistema Jarvis.

---

## 2. Papéis oficiais

## 2.1 Alpha

Alpha é responsável por:

- gênese
- identidade raiz
- prova de origem
- avaliação de pré-existência
- contrato de fronteira com o ecossistema

Alpha não é responsável por:

- runtime
- backlog operacional
- sessão
- recovery operacional
- deploy

## 2.2 State

State é responsável por:

- governança canônica
- guardrails
- memória curada
- registries institucionais
- reconciliação de verdade entre camadas

## 2.3 Omega

Omega é responsável por:

- lifecycle de sessão
- replay
- recovery
- lineage de continuidade entre ciclos de trabalho

## 2.4 Codex/Ruptur

Ruptur é responsável por:

- manifestação operacional
- execução viva
- connectome
- automações e operação do ecossistema

---

## 3. Relações entre os repositórios

## 3.1 Alpha -> State

Alpha fornece a identidade raiz que o State governa institucionalmente.

## 3.2 State -> Alpha

State valida, reconcilia e preserva a camada canônica que impede que Alpha seja reescrito por improviso operacional.

## 3.3 Alpha -> Omega

Alpha fornece os invariantes de identidade que sessões e recoveries não podem quebrar.

## 3.4 Omega -> Alpha

Omega deve tratar a identidade do Alpha como âncora, não como variável efêmera.

## 3.5 Alpha -> Ruptur

Alpha fornece a origem pública da entidade manifestada operacionalmente.

## 3.6 Ruptur -> Alpha

Ruptur manifesta e opera, mas não redefine a gênese nem a soberania da identidade raiz.

---

## 4. Regras de não-interferência

1. Alpha não substitui State.  
2. State não vira runtime.  
3. Omega não cria nova entidade por sessão.  
4. Ruptur não redefine identidade canônica por conveniência operacional.

---

## 5. Regra de conflito entre fontes

Quando houver conflito entre:

- documentação de gênese
- governança canônica
- runtime operacional
- sessão/recovery
- espelhos locais

o conflito deve ser classificado e reconciliado de forma explícita.

Não é permitido:

- promover automaticamente a fonte mais recente
- assumir que runtime vence governança
- assumir que sessão vence gênese

---

## 6. Resultado esperado

Com este contrato:

- Alpha ancora
- State governa
- Omega continua
- Ruptur opera

