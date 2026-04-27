# 🧪 Casos de Teste — Sistema de Denúncia de Lixo (Tianguá)

---

## ✅ CT-01 — Envio de denúncia com sucesso

**Cenário:** Enviar denúncia preenchendo todos os campos obrigatórios

| Passo | Ação |
|-------|------|
| **Dado** | que o usuário acessa o sistema de denúncia |
| **Quando** | ele seleciona um tipo de ocorrência |
| **E** | informa o bairro |
| **E** | preenche a rua ou referência |
| **E** | descreve a ocorrência |
| **E** | seleciona o nível de urgência |
| **E** | aciona o botão "Enviar denúncia" |
| **Então** | o sistema deve registrar a denúncia com sucesso |
| **E** | exibir um número de protocolo |
| **E** | apresentar o modal de confirmação |

---

## ❌ CT-02 — Tentativa de envio sem tipo de ocorrência

**Cenário:** Validar envio sem seleção de tipo

| Passo | Ação |
|-------|------|
| **Dado** | que o usuário acessa o sistema |
| **Quando** | ele preenche todos os campos obrigatórios exceto o tipo de ocorrência |
| **E** | aciona "Enviar denúncia" |
| **Então** | o sistema deve exibir uma mensagem solicitando a seleção do tipo |

---

## ❌ CT-03 — Tentativa de envio sem bairro

**Cenário:** Validar envio sem bairro

| Passo | Ação |
|-------|------|
| **Dado** | que o usuário acessa o sistema |
| **Quando** | ele preenche todos os campos obrigatórios exceto o bairro |
| **E** | aciona "Enviar denúncia" |
| **Então** | o sistema deve exibir mensagem solicitando o bairro |

---

## ❌ CT-04 — Tentativa de envio sem descrição

**Cenário:** Validar envio sem descrição

| Passo | Ação |
|-------|------|
| **Dado** | que o usuário acessa o sistema |
| **Quando** | ele não preenche o campo de descrição |
| **E** | aciona "Enviar denúncia" |
| **Então** | o sistema deve exibir mensagem solicitando a descrição da ocorrência |

---

## ❌ CT-05 — Tentativa de envio sem nível de urgência

**Cenário:** Validar envio sem urgência

| Passo | Ação |
|-------|------|
| **Dado** | que o usuário acessa o sistema |
| **Quando** | ele preenche todos os campos obrigatórios exceto o nível de urgência |
| **E** | aciona "Enviar denúncia" |
| **Então** | o sistema deve exibir mensagem solicitando o nível de urgência |

---

## 📷 CT-06 — Upload de imagens

**Cenário:** Adicionar fotos à denúncia

| Passo | Ação |
|-------|------|
| **Dado** | que o usuário acessa o sistema |
| **Quando** | ele seleciona uma ou mais imagens |
| **Então** | o sistema deve exibir o preview das imagens carregadas |

---

## 🧹 CT-07 — Limpeza do formulário após envio

**Cenário:** Resetar formulário após envio

| Passo | Ação |
|-------|------|
| **Dado** | que o usuário realizou uma denúncia com sucesso |
| **Quando** | ele aciona "Fazer nova denúncia" |
| **Então** | o formulário deve ser limpo |
| **E** | todos os campos devem retornar ao estado inicial |

---

## 📍 CT-08 — Obter localização do usuário

**Cenário:** Capturar localização atual

| Passo | Ação |
|-------|------|
| **Dado** | que o usuário acessa o sistema |
| **Quando** | ele aciona "Usar minha localização atual" |
| **Então** | o sistema deve solicitar permissão de localização |
| **E** | exibir as coordenadas capturadas |

---

## 🚫 CT-09 — Negar permissão de localização

**Cenário:** Usuário nega acesso à localização

| Passo | Ação |
|-------|------|
| **Dado** | que o usuário acessa o sistema |
| **Quando** | ele nega a permissão de localização |
| **Então** | o sistema deve exibir mensagem informando falha ao obter localização |
