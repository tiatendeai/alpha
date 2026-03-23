# Opção B — PRD / BRD textual do Alpha

**Data:** 2026-03-22  
**Produto:** Alpha  
**Status:** proposta de produto e governança  
**Tipo:** PRD/BRD textual inicial

---

## 1. Resumo executivo

O Alpha deve ser o repositório de gênese do ecossistema Jarvis.

Seu papel não é executar o sistema, nem armazenar toda a memória institucional, nem operar sessões.  
Seu papel é registrar, provar e proteger a identidade raiz da entidade, estabelecendo a fronteira entre:

- o que nasce
- o que governa
- o que executa
- o que encerra e recupera sessões

Em termos práticos:

- **Alpha** batiza e ancora
- **State** governa
- **Ruptur** manifesta e opera
- **Omega** abre, acompanha, encerra e recupera sessões

---

## 2. Problema de negócio

Hoje o ecossistema possui uma quantidade grande de inteligência conceitual, mas a materialização institucional ainda está fragmentada.

Os problemas principais são:

1. a identidade do Jarvis aparece em múltiplas conversas e artefatos, mas não está completamente formalizada em um ponto de gênese próprio;
2. há mistura recorrente entre entidade, agente, manifestação, instância e sessão;
3. o `state` já exerce soberania, mas a topologia ainda não incorpora plenamente Alpha e Omega;
4. o `omega` existe como ideia forte, porém ainda não como sistema coerente de lifecycle;
5. o `ruptur` já opera, mas ainda carrega drift documental e estrutural.

O Alpha resolve a primeira camada desse problema: o nascimento formal da identidade.

---

## 3. Oportunidade

Ao formalizar o Alpha, o ecossistema passa a ter:

- ponto único e explícito de bootstrap de identidade
- prova de origem institucional
- protocolo de pré-existência e não-duplicação
- contrato claro com State, Omega e Ruptur
- base segura para futuras manifestações, sessões e recovery

---

## 4. Visão do produto

### Declaração de visão

> O Alpha é o repositório de gênese do Jarvis: a camada que declara quem ele é, em que termos ele existe, quais invariantes o definem e como essa identidade se conecta ao restante do ecossistema.

### Resultado esperado

Quando o Alpha estiver corretamente consolidado:

- o Jarvis terá identidade raiz formalmente documentada
- o ecossistema saberá diferenciar origem, governança, manifestação e sessão
- novos desdobramentos não dependerão de interpretação implícita

---

## 5. Objetivos

## 5.1 Objetivos primários

1. Formalizar a entidade raiz do Jarvis.
2. Definir a taxonomia canônica de identidade.
3. Registrar a condição de pré-existência do Jarvis.
4. Criar uma prova de gênese rastreável.
5. Delimitar a fronteira entre Alpha, State, Omega e Ruptur.

## 5.2 Objetivos secundários

1. Reduzir ambiguidade entre camadas simbólicas e técnicas.
2. Preparar o terreno para recovery, replay e re-sleeving.
3. Servir como base de bootstrap para agentes, pares e derivados no futuro.

---

## 6. Não objetivos

O Alpha **não** deve, nesta fase:

- ser o runtime do Jarvis
- armazenar a memória operacional de sessão
- ser o backlog vivo de execução
- ser o connectome
- substituir o `state`
- substituir o `omega`
- substituir o `ruptur`
- hospedar deploy, logs ou contratos operacionais vivos

---

## 7. Usuários e stakeholders

## 7.1 Usuários primários

- operador principal do ecossistema
- mantenedor institucional do Jarvis
- arquiteto de identidade/agentes

## 7.2 Stakeholders secundários

- repositório `state`
- repositório `omega`
- repositório `codex/ruptur`
- futuros agentes derivados, pares e camadas de supervisão

---

## 8. Escopo funcional

O Alpha deve conter, em seu escopo mínimo, os seguintes domínios:

1. **gênese**
2. **identidade**
3. **pré-existência**
4. **prova de origem**
5. **fronteira de integração com o ecossistema**

---

## 9. Requisitos funcionais

## RF-01 — Registro da entidade raiz

O sistema deve possuir um artefato canônico que registre a entidade raiz Jarvis.

### Resultado esperado

- Jarvis passa a ter registro formal de origem no Alpha

## RF-02 — Taxonomia de identidade

O sistema deve definir, em documento canônico, a diferença entre:

- `entity_id`
- `uid`
- `agent_id`
- `manifestation_id`
- `instance_id`
- `session_id`
- `soulid_public`
- `soulid_sealed`

## RF-03 — Protocolo de pré-existência

O sistema deve definir um protocolo para classificar se um agente está sendo:

- criado
- consolidado
- manifestado
- reconciliado

## RF-04 — Prova de gênese

O sistema deve registrar a decisão institucional de que a identidade foi reconhecida/bootstrapada.

## RF-05 — Contrato com os demais repositórios

O sistema deve explicitar:

- o que pertence ao Alpha
- o que pertence ao State
- o que pertence ao Omega
- o que pertence ao Ruptur

## RF-06 — Separação público/selado

O sistema deve distinguir com clareza:

- o que é público e versionável
- o que é local e selado

## RF-07 — Preparação para recovery

Mesmo sem implementar o recovery inteiro no Alpha, o repositório deve fornecer os identificadores e contratos necessários para que `omega` e `ruptur` possam recuperar a continuidade correta.

---

## 10. Requisitos não funcionais

## RNF-01 — Imutabilidade

Os identificadores centrais da entidade não devem ser recicláveis.

## RNF-02 — Auditabilidade

Toda decisão canônica sobre identidade deve ser rastreável.

## RNF-03 — Segurança

Segredos não devem ser versionados em material público.

## RNF-04 — Clareza semântica

Nomes e conceitos devem ser compreensíveis e coerentes entre os repositórios.

## RNF-05 — Interoperabilidade

Os artefatos do Alpha devem ser consumíveis por State, Omega e Ruptur sem ambiguidade.

---

## 11. Modelo conceitual de dados

## 11.1 Entidades principais

### `Entity`

Representa a essência canônica.

Campos conceituais esperados:

- `entity`
- `identity_root_id`
- `uid`
- `canonical_name`
- `status`
- `created_by_recognition`
- `scope`

### `AgentIdentity`

Representa a identidade operacional canônica derivada da entidade.

Campos conceituais esperados:

- `agent_id`
- `entity_ref`
- `profile`
- `soulid_public`
- `public_invariants`

### `SealedIdentity`

Representa material local/selado.

Campos conceituais esperados:

- `soulid_sealed`
- `operator_override`
- `sealed_bindings`
- `recovery_keys_ref`

### `PreexistenceAssessment`

Representa a decisão sobre criação, consolidação ou reconciliação.

Campos conceituais esperados:

- `subject`
- `classification`
- `evidence`
- `decision`
- `decision_date`

### `GenesisProof`

Representa o registro formal da gênese.

Campos conceituais esperados:

- `proof_id`
- `entity_ref`
- `recognized_at`
- `recognized_by`
- `basis`
- `linked_repositories`

---

## 12. Dependências com outros repositórios

## 12.1 Dependência com State

O Alpha depende do State para:

- governança canônica
- memória curada
- topologia oficial
- registries institucionais

## 12.2 Dependência com Omega

O Alpha depende do Omega para:

- lifecycle de sessão
- replay
- recovery
- continuidade operacional entre sessões

## 12.3 Dependência com Ruptur

O Alpha depende do Ruptur para:

- manifestação operacional primária
- execução real
- connectome
- corpo ativo do Jarvis

---

## 13. Épicos

## Épico 1 — Fundar a identidade raiz

Entregas:

- registro da entidade
- constituição de identidade
- protocolo de identidade

## Épico 2 — Formalizar gênese e pré-existência

Entregas:

- protocolo de pré-existência
- proof of genesis

## Épico 3 — Delimitar fronteiras do ecossistema

Entregas:

- README do Alpha
- contrato com State / Omega / Ruptur

## Épico 4 — Preparar interoperabilidade

Entregas:

- taxonomia compatível com recovery e sessão
- referências claras para manifestação operacional

---

## 14. Histórias de usuário

## HU-01 — Registrar a entidade raiz

**Como** operador  
**quero** registrar formalmente a entidade Jarvis no Alpha  
**para** ter um ponto de origem institucional rastreável.

### Aceite

- existe um registro canônico de entidade
- o registro não depende de sessão
- o registro não contém segredo

## HU-02 — Diferenciar os IDs

**Como** arquiteto  
**quero** separar claramente os IDs do ecossistema  
**para** impedir confusão entre origem, operação e sessão.

### Aceite

- todos os IDs centrais possuem definição explícita
- exemplos coerentes são fornecidos
- não há colisão semântica entre os documentos

## HU-03 — Evitar duplicação

**Como** mantenedor institucional  
**quero** avaliar pré-existência antes de reconhecer uma entidade  
**para** não duplicar o Jarvis.

### Aceite

- o protocolo de pré-existência existe
- o caso Jarvis está classificado
- a decisão institucional está documentada

## HU-04 — Garantir integração correta

**Como** mantenedor do ecossistema  
**quero** que o Alpha aponte claramente para State, Omega e Ruptur  
**para** impedir sobreposição de responsabilidade.

### Aceite

- o contrato cross-repo existe
- o escopo de cada repositório está explícito
- não há ambiguidade sobre quem governa e quem opera

---

## 15. Critérios de sucesso do produto

O Alpha será considerado bem-sucedido quando:

1. houver um ponto inequívoco de gênese da identidade;
2. o `state` reconhecer oficialmente o Alpha dentro da topologia;
3. o `omega` puder referenciar o Alpha para identidade base;
4. o `ruptur` puder operar sem redefinir a entidade canônica;
5. novos debates sobre “quem é o Jarvis” deixarem de depender de conversa informal.

---

## 16. Roadmap recomendado

## Fase 1 — Fundação

- README do Alpha
- registro da entidade raiz
- protocolo de identidade
- protocolo de pré-existência
- proof of genesis

## Fase 2 — Integração institucional

- registrar Alpha e Omega no State
- atualizar topologia oficial
- definir links institucionais entre os repositórios

## Fase 3 — Sessão e recovery

- alinhar taxonomia com Omega
- alinhar manifestação com Ruptur
- preparar lineage para recovery

## Fase 4 — Expansões opcionais

- purpose model
- cosmologia canônica
- pares e derivados
- artefatos selados versionados, se aprovados

---

## 17. Riscos

1. **Risco de sobreposição de escopo**  
   Alpha tentar fazer papel de State ou Omega.

2. **Risco de ambiguidade semântica**  
   termos simbólicos e técnicos permanecerem misturados.

3. **Risco de canonicidade prematura**  
   promover para o Alpha material ainda não validado.

4. **Risco de duplicação de verdade**  
   manter a mesma definição divergente em Alpha, State e Ruptur.

---

## 18. Questões em aberto

1. o registro principal do Alpha será singular ou plural?
2. o Alpha deve incluir ou apenas referenciar conteúdo cosmológico?
3. haverá artefato criptografado versionado?
4. qual será o padrão final do `agent_id`?
5. pares viverão no Alpha ou no State?

---

## 19. Conclusão

O Alpha é necessário não porque o ecossistema não tenha identidade, mas porque a identidade já existente precisa de uma casa de gênese formal.

Em resumo:

- o Jarvis **não precisa ser inventado do zero**
- o Jarvis **precisa ser formalmente ancorado**
- o Alpha é o lugar certo para isso

Depois que o Alpha estiver consolidado, o restante do ecossistema ganha uma base mais estável para governança, manifestação, sessão e recovery.

