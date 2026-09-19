# 🚀 Desafio Criativo: Planejando Automações com N8N

Este repositório contém o planejamento estratégico e a engenharia de prompt para a construção de um fluxo de trabalho automatizado utilizando a ferramenta **N8N**.

---

## 📝 Prompt Final Estruturado

Atue como um especialista em N8N.

Crie uma automação para registrar leads recebidos por formulário.

### 👥 Público:
Equipe comercial.

### 🛠️ Ferramentas envolvidas:
Google Forms, Google Sheets e Gmail.

### 🔄 Fluxo:
Receber uma resposta, salvar os dados na planilha e enviar um e-mail de confirmação.

### ⚠️ Regras:
Ignorar registros sem e-mail válido.

---

## ⚙️ Arquitetura do Workflow Sugerida

Para executar este projeto no N8N, a lógica de funcionamento deve utilizar os seguintes nós principais:

1. **Google Forms Trigger (ou Webhook Node):** Responsável por iniciar o fluxo instantaneamente assim que um novo lead preencher o formulário.
2. **Filter Node (ou If Node):** Validará o campo de e-mail usando uma expressão regular (Regex) para garantir que apenas cadastros com e-mails válidos continuem no fluxo.
3. **Google Sheets Node:** Configurado na ação *Append Row* para inserir as informações validadas do lead nas colunas correspondentes da planilha da equipe comercial.
4. **Gmail Node:** Configurado na ação *Send Email* para disparar a mensagem de confirmação personalizada utilizando os dados capturados do lead (como nome e e-mail).

---
*Desafio desenvolvido como parte da formação em automação e inteligência artificial.*
