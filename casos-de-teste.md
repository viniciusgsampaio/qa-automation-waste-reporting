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

### Evidências

![CT-01 evidência 1](evidencias/image1.png)
![CT-01 evidência 2](evidencias/image2.png)
![CT-01 evidência 3](evidencias/image3.png)

---

## ❌ CT-02 — Tentativa de envio sem tipo de ocorrência

**Cenário:** Validar envio sem seleção de tipo

| Passo | Ação |
|-------|------|
| **Dado** | que o usuário acessa o sistema |
| **Quando** | ele preenche todos os campos obrigatórios exceto o tipo de ocorrência |
| **E** | aciona "Enviar denúncia" |
| **Então** | o sistema deve exibir uma mensagem solicitando a seleção do tipo |

### Evidências

![CT-02 evidência 1](evidencias/image4.png)
![CT-02 evidência 2](evidencias/image5.png)

---

## ❌ CT-03 — Tentativa de envio sem bairro

**Cenário:** Validar envio sem bairro

| Passo | Ação |
|-------|------|
| **Dado** | que o usuário acessa o sistema |
| **Quando** | ele preenche todos os campos obrigatórios exceto o bairro |
| **E** | aciona "Enviar denúncia" |
| **Então** | o sistema deve exibir mensagem solicitando o bairro |

### Evidências

![CT-03 evidência 1](evidencias/image6.png)
![CT-03 evidência 2](evidencias/image7.png)

---

## ❌ CT-04 — Tentativa de envio sem descrição

**Cenário:** Validar envio sem descrição

| Passo | Ação |
|-------|------|
| **Dado** | que o usuário acessa o sistema |
| **Quando** | ele não preenche o campo de descrição |
| **E** | aciona "Enviar denúncia" |
| **Então** | o sistema deve exibir mensagem solicitando a descrição da ocorrência |

### Evidências

![CT-04 evidência 1](evidencias/image8.png)
![CT-04 evidência 2](evidencias/image9.png)

---

## ❌ CT-05 — Tentativa de envio sem nível de urgência

**Cenário:** Validar envio sem urgência

| Passo | Ação |
|-------|------|
| **Dado** | que o usuário acessa o sistema |
| **Quando** | ele preenche todos os campos obrigatórios exceto o nível de urgência |
| **E** | aciona "Enviar denúncia" |
| **Então** | o sistema deve exibir mensagem solicitando o nível de urgência |

### Evidências

![CT-05 evidência 1](evidencias/image10.png)
![CT-05 evidência 2](evidencias/image11.png)

---

## 📷 CT-06 — Upload de imagens

**Cenário:** Adicionar fotos à denúncia

| Passo | Ação |
|-------|------|
| **Dado** | que o usuário acessa o sistema |
| **Quando** | ele seleciona uma ou mais imagens |
| **Então** | o sistema deve exibir o preview das imagens carregadas |

### Evidências

![CT-06 evidência 1](evidencias/image12.png)

---

## 🧹 CT-07 — Limpeza do formulário após envio

**Cenário:** Resetar formulário após envio

| Passo | Ação |
|-------|------|
| **Dado** | que o usuário realizou uma denúncia com sucesso |
| **Quando** | ele aciona "Fazer nova denúncia" |
| **Então** | o formulário deve ser limpo |
| **E** | todos os campos devem retornar ao estado inicial |

### Evidências

![CT-07 evidência 1](evidencias/image13.png)
![CT-07 evidência 2](evidencias/image14.png)

---

## 📍 CT-08 — Obter localização do usuário

**Cenário:** Capturar localização atual

| Passo | Ação |
|-------|------|
| **Dado** | que o usuário acessa o sistema |
| **Quando** | ele aciona "Usar minha localização atual" |
| **Então** | o sistema deve solicitar permissão de localização |
| **E** | exibir as coordenadas capturadas |

### Evidências

![CT-08 evidência 1](evidencias/image15.png)
![CT-08 evidência 2](evidencias/image16.png)

---

## 🚫 CT-09 — Negar permissão de localização

**Cenário:** Usuário nega acesso à localização

| Passo | Ação |
|-------|------|
| **Dado** | que o usuário acessa o sistema |
| **Quando** | ele nega a permissão de localização |
| **Então** | o sistema deve exibir mensagem informando falha ao obter localização |

### Evidências

![CT-09 evidência 1](evidencias/image17.png)
![CT-09 evidência 2](evidencias/image18.png)
