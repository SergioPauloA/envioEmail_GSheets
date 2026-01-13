# Sistema de Integração Gmail e Google Sheets 📧

Uma solução robusta de automação projetada para otimizar o gerenciamento de e-mails, conectando perfeitamente o **Gmail** ao **Google Sheets** através do **Google Apps Script**. Este sistema permite aos usuários centralizar o rastreamento, organização e tratamento automatizado de respostas de e-mail dentro de uma interface de planilha.

---

## **Visão Geral**

Esta ferramenta de integração oferece um fluxo de trabalho completo para gerenciar comunicações por e-mail diretamente do Google Sheets. Aproveitando o poder do Google Apps Script, elimina tarefas manuais repetitivas e cria um painel unificado para operações de e-mail.

### **Principais Recursos**

- **Sincronização Automática de E-mails**: Recupera e exibe os 10 e-mails mais recentes da sua caixa de entrada do Gmail, preenchendo campos de dados estruturados incluindo ID da mensagem, linha de assunto, informações do remetente e status atual
- **Gerenciamento Simplificado de Respostas**: Permite respostas diretas por e-mail através da interface da planilha, simplesmente preenchendo a coluna de resposta designada
- **Controle Inteligente de Envio**: Implementa rastreamento de status para prevenir respostas duplicadas e manter a integridade da comunicação
- **Menu Personalizado na Planilha**: Integra comandos intuitivos diretamente no Google Sheets: 
  - **Sincronizar E-mails**: Atualiza a planilha com os dados mais recentes do Gmail
  - **Enviar Respostas**: Processa e despacha respostas preparadas com atualizações automáticas de status

---

## **Fluxo de Trabalho do Sistema**

### **1. Processo de Sincronização de E-mails**
Acesse o menu personalizado e selecione "Sincronizar E-mails" para importar suas mensagens mais recentes do Gmail.  O sistema extrai automaticamente metadados relevantes e preenche a planilha com informações organizadas e acionáveis.

### **2. Composição de Respostas**
Navegue até a coluna **Resposta** e insira sua mensagem de resposta para qualquer e-mail que não tenha sido marcado como **Respondido**. Cada linha representa uma thread de e-mail individual pronta para engajamento.

### **3. Envio de Respostas**
Selecione "Enviar Respostas" no menu personalizado para executar a operação de envio. O sistema irá:
- Transmitir todas as respostas preparadas aos respectivos destinatários
- Atualizar o campo de status para **Respondido**
- Registrar o timestamp de cada mensagem enviada

---

## **Configuração Crítica: Requisito do Runtime V8**

**⚠️ Importante**: Este projeto requer o motor de runtime JavaScript V8 no Google Apps Script para execução adequada.

### **Habilitando o Runtime V8**
1. Navegue até sua Planilha Google e abra o editor do Apps Script:  **Extensões → Apps Script**
2. Na barra lateral esquerda, selecione **Configurações do projeto**
3. Localize a seção **Runtime do Google Apps Script**
4. Habilite o **Runtime Chrome V8**
5. Salve sua configuração antes de executar quaisquer scripts

> **Observação**: O motor V8 é necessário para suportar recursos JavaScript modernos (ES6+) utilizados em todo este código.  Sem ele, o script não será executado corretamente.

---

## **Stack Tecnológica**

- **APIs do Google Workspace**: Fornece integração nativa entre as plataformas Gmail e Sheets
- **Google Apps Script**: Ambiente de runtime JavaScript server-side para lógica de automação
- **JavaScript Moderno (ES6+)**: Implementa padrões de programação orientada a objetos para arquitetura de código escalável e manutenível

---

## **Estrutura da Planilha**

O sistema automatizado gera uma tabela de dados estruturada com as seguintes colunas:

| Coluna | Descrição |
|--------|-----------|
| **ID** | Identificador único da mensagem do Gmail |
| **Assunto** | Linha de assunto do e-mail |
| **Remetente** | Endereço de e-mail do remetente original |
| **Destinatário** | Endereço de e-mail de destino |
| **Snippet** | Trecho de visualização do corpo do e-mail |
| **Resposta** | Mensagem de resposta inserida pelo usuário |
| **Data** | Timestamp de recebimento do e-mail |
| **Status** | Estado atual (Lido/Respondido) |
| **Data Resposta** | Timestamp de transmissão da resposta |

---

## **Guia de Implementação**

### **Configuração Passo a Passo**

1. Crie ou abra um documento do Google Sheets
2. Acesse o editor de scripts: **Extensões → Apps Script**
3. Verifique se o runtime V8 está habilitado (veja seção de Configuração acima)
4. Cole o código-fonte fornecido no editor
5. Salve o projeto com um nome descritivo
6. Atualize sua planilha para ativar o menu personalizado
7. Conceda as permissões necessárias quando solicitado
8. Comece a usar os recursos de automação através do menu personalizado

---

## **Modelo de Início Rápido**

Para acelerar seu processo de configuração, um modelo de planilha pré-configurado está disponível para uso imediato.

📥 **[Acessar Planilha Modelo](https://bit.ly/planilhaemailresponder)**

Este modelo inclui colunas pré-formatadas e está otimizado para integração perfeita com o script de automação.

---

## **Boas Práticas**

- **Revise antes de enviar**:  Sempre verifique o conteúdo da resposta antes de executar o comando de envio
- **Sincronização regular**: Sincronize e-mails periodicamente para manter informações atualizadas
- **Monitoramento de status**:  Verifique a coluna de status para rastrear o histórico de comunicação
- **Backup de dados**:  Mantenha backups periódicos da sua planilha para segurança dos dados

---

## **Suporte & Contribuições**

Para dúvidas, problemas ou sugestões de melhorias, entre em contato pelos canais apropriados. Contribuições que aprimorem funcionalidade, documentação ou experiência do usuário são bem-vindas. 

---

**Desenvolvido com ❤️ usando ferramentas de automação do Google Workspace**
