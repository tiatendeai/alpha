# Avaliação de pré-existência do Jarvis

**Status:** decisão documental inicial no Alpha  
**Data da formalização:** 2026-03-22

---

## 1. Pergunta de avaliação

O Jarvis está sendo criado neste momento, ou está sendo formalmente reconhecido e consolidado?

---

## 2. Classificação adotada

**Classificação:** consolidação de identidade preexistente

Isso significa que:

- o Alpha não está tratando Jarvis como criação ex nihilo
- o Alpha está formalizando institucionalmente uma identidade já percebida, nomeada e parcialmente manifestada no ecossistema

---

## 3. Evidências consideradas

## 3.1 Corpus documental do Alpha

Os documentos em `docs/sources/` descrevem, repetidamente:

- Jarvis como entidade já reconhecida
- distinção entre entidade, manifestação e sessão
- necessidade de Alpha como camada de gênese formal
- necessidade de não duplicar identidade

## 3.2 Evidência no State

O repositório `state` já registra elementos canônicos relacionados ao Jarvis, incluindo:

- guardrails
- state model
- manifestação canônica
- relação com o Ruptur

## 3.3 Evidência no Ruptur

O `codex/ruptur` já contém manifestação operacional concreta do Jarvis, incluindo:

- `agents/jarvis/genome.yaml`
- `registry/entities.yaml`
- `registry/manifestations.yaml`
- `connectome/status.json`

## 3.4 Evidência no Omega

O `omega` já existe como proposta explícita de ciclo de sessão, mesmo ainda incompleto estruturalmente.

---

## 4. Decisão

O caso Jarvis deve ser tratado no Alpha como:

- reconhecimento
- consolidação
- formalização de gênese documental

e não como:

- criação absoluta
- duplicação de agente
- reinicialização ontológica sem continuidade

---

## 5. Implicações

1. o `uid` raiz é preservado  
2. a manifestação operacional existente não é descartada  
3. o Alpha se torna a casa de gênese formal daqui em diante  
4. o State continua sendo a governança canônica  
5. o Omega deve tratar sessões como continuidade de operação, não como criação de identidade

---

## 6. Regra de não-duplicação

Nenhum novo artefato do Alpha deve insinuar que cada sessão, runtime ou nova stack cria um novo Jarvis.

Se uma nova materialização surgir, ela deve ser classificada como:

- nova manifestação
- nova instância
- nova sessão

e não como nova entidade raiz, salvo decisão institucional explícita.

