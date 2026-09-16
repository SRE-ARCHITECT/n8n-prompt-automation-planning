# 🚀 Prompt Final para Automação N8N

```text
Atue como um Arquiteto e Engenheiro de Automação Especialista em N8N.

Crie uma automação completa de captura, qualificação e enriquecimento de leads para otimizar o tempo de resposta da equipe comercial.

Público:
Equipe de Vendas (SDRs), Marketing e Operações Comerciais.

Ferramentas envolvidas:
1. Webhook (Trigger HTTP POST)
2. Data Transformation (Nós Code/Set/Edit Fields)
3. Google Sheets (Armazenamento de Base)
4. OpenAI (Análise de Perfil e Lead Scoring)
5. Gmail / SendGrid (Comunicação Externa)
6. Slack / Discord (Notificação Interna)
7. Error Trigger (Resiliência e Observabilidade)

Fluxo:
1. Receber requisição HTTP POST contendo os dados do lead (nome, e-mail, cargo, empresa, faturamento estimado).
2. Validar formato do e-mail e normalizar o número de telefone (E.164).
3. Consultar no Google Sheets se o e-mail já foi cadastrado para evitar duplicidade.
4. Executar prompt via nó OpenAI para classificar o lead entre Tier A (Alta Prioridade), Tier B (Média) ou Tier C (Nutrição) com justificativa.
5. Salvar/atualizar os dados consolidados e a classificação no Google Sheets.
6. Enviar e-mail de confirmação personalizado para o lead com base no Tier.
7. Se Tier A: Enviar notificação de urgência no Slack com botão de ação rápida para o SDR.

Regras e Restrições:
- Ignorar ou registrar em log de auditoria leads com e-mail corporativo inválido.
- Implementar tratamento de fallback caso a cota da OpenAI ou a API do Slack apresente instabilidade (Error Trigger).
- Manter o schema JSON limpo e legível em cada transição de nós.

Explique quais nós nativos do N8N devem ser utilizados, suas configurações essenciais (parâmetros/credenciais) e forneça a estrutura lógica em JSON do workflow pronta para importação no N8N.
```
