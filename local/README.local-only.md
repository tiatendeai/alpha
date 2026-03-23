# Regras para material local e selado

Este diretório existe apenas para documentar o que **pode existir localmente**, mas **não deve ser versionado como segredo no repositório**.

---

## 1. O que é material local/selado

Exemplos:

- `soulid_sealed` real
- chaves
- credenciais
- binds sensíveis
- overrides operacionais sensíveis
- referências privadas de recovery

---

## 2. O que nunca deve ser commitado

Não deve ser commitado no Alpha:

- segredo em texto puro
- arquivo de chave
- token
- credencial
- material criptográfico sensível
- valor real de `soulid_sealed`

---

## 3. Relação com `operator_override`

`operator_override` deve ser tratado como mecanismo operacional temporário.

Ele não deve:

- redefinir a entidade Jarvis
- alterar o `uid`
- substituir a governança canônica

---

## 4. Regra prática

Se um arquivo local contiver informação que cause risco se for pública, ele deve permanecer:

- fora do Git
- ou explicitamente ignorado
- ou armazenado em camada segura apropriada

---

## 5. Escopo deste diretório

Este diretório, por si só, não é o cofre de segredos do ecossistema.  
Ele apenas documenta a política de separação entre:

- público/versionável
- local/selado

