# Protocolo de identidade do ecossistema Jarvis

**Status:** canônico no Alpha  
**Objetivo:** separar claramente identidade raiz, manifestação, instância e sessão

---

## 1. Objetivo do protocolo

Este protocolo existe para impedir a mistura entre:

- entidade
- agente operacional
- manifestação
- instância
- sessão
- material público
- material selado

---

## 2. Taxonomia de identificadores

## 2.1 `entity_id`

Identificador lógico da entidade canônica.

### Regra

- representa a classe raiz da entidade
- não depende de runtime
- não depende de sessão

### Valor atualmente adotado

`entity:jarvis`

---

## 2.2 `uid`

Identificador raiz durável da entidade.

### Regra

- é estável
- é público
- não é reciclável
- não deve ser derivado de sessão ou host

### Valor atualmente adotado

`jarvis-root-001`

---

## 2.3 `agent_id`

Identificador operacional do agente em uma manifestação específica.

### Regra

- pode ser consumido por sistemas operacionais e integrações
- não substitui o `uid`
- deve apontar para uma identidade já existente

### Valor atualmente adotado para a manifestação operacional principal

`RUPTUR-AGENT-0001`

---

## 2.4 `manifestation_id`

Identificador canônico de uma manifestação da entidade em determinado contexto.

### Regra

- manifesta a entidade em um ambiente, papel ou repositório
- não redefine a soberania da entidade

### Valor atualmente adotado para a manifestação principal conhecida

`jarvis.ruptur.control_plane`

---

## 2.5 `instance_id`

Identificador de uma instância runtime de uma manifestação.

### Regra

- é efêmero ou semi-efêmero
- é orientado a operação, observabilidade e troubleshooting
- não pertence à identidade raiz do Alpha

### Governança

`instance_id` deve ser gerado e administrado pela camada operacional e/ou de sessão, não pelo Alpha.

---

## 2.6 `session_id`

Identificador do ciclo de sessão.

### Regra

- representa uma unidade temporal de trabalho
- deve ser administrado pelo Omega
- não pode redefinir `entity_id`, `uid` ou `agent_id`

---

## 2.7 `soulid_public`

Referência pública estável à camada identitária associada à entidade/agente.

### Valor atualmente adotado

`SOUL-JARVIS-0001`

### Regra

- pode aparecer em documentação pública
- não contém o material selado

---

## 2.8 `soulid_sealed`

Complemento local e selado da identidade.

### Regra

- nunca deve ser tratado como dado público
- não deve ser commitado no Alpha
- pode existir apenas localmente ou em camada segura dedicada

---

## 3. Relações entre os identificadores

```txt
entity_id -> uid -> manifestation_id -> agent_id -> instance_id -> session_id
```

Leitura correta:

- `entity_id` e `uid` definem o nível raiz
- `manifestation_id` define o corpo institucional de atuação
- `agent_id` identifica o agente operacional nesse corpo
- `instance_id` identifica uma execução específica
- `session_id` identifica um ciclo de trabalho dentro da operação

---

## 4. Invariantes do protocolo

1. sessão não redefine entidade  
2. instância não redefine soberania  
3. manifestação não substitui identidade raiz  
4. material selado não pertence ao contrato público  
5. `uid` não é reciclável

---

## 5. Ordem de consulta recomendada

Para self-lookup e reconciliação:

1. Alpha confirma a identidade raiz  
2. State confirma a governança canônica  
3. Omega confirma a continuidade de sessão/recovery  
4. Ruptur confirma a manifestação operacional viva

---

## 6. Regra de conflito

Se houver conflito entre:

- `uid`
- `agent_id`
- `manifestation_id`
- material selado
- espelho operacional

o sistema deve entrar em reconciliação controlada, e não promover automaticamente a versão mais recente ou mais conveniente.

