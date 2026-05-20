#  Sprint 2 - GoodWe - Chatbot
Chatbot com IA para gestão de eletropostos em condomínios (EV ChargeOps) – Desafio GoodWe & FIAP 2026.
 
##  Integrantes
* **Daniel Vieira Santos** - RM: 573326
* **Gustavo Bitencourt Lopes** - RM: 568885
* **Giovane Salazar Fioravante** - RM: 570396
* **Leonardo Basile Takachi** - RM: 569066
 
## Problema
No contexto do EV Challenge 2026, o cenário EV ChargeOps apresenta a ausência de mecanismos inteligentes para gerenciar o uso compartilhado de eletropostos em condomínios. Síndicos enfrentam dificuldades para:
 
- Controlar o consumo individual de energia por unidade
- Realizar o rateio correto de custos
- Monitorar o uso das estações
- Identificar falhas técnicas nos carregadores
 
Essa falta de automação gera erros operacionais, retrabalho e baixa eficiência na gestão.
 
##  Tecnologias Selecionadas
* **Linguagem:** Python
  * *Justificativa:* Utilizado pela versatilidade e robustez no tratamento de dados e integração de APIs.
* **IA/LLM:** Google Gemini API
  * *Justificativa:* Escolhido pela alta capacidade de interpretar linguagem natural e gerar respostas contextualizadas com base em dados operacionais de contexto e integração nativa com ferramentas de análise.
* **Análise de Dados:** Pandas
  * *Justificativa:* Biblioteca essencial para simular a leitura de bancos de dados de consumo e gerar relatórios precisos para o síndico.
* **Interface:** Streamlit ou Flask
  * *Justificativa:* Para garantir uma interface de usuário (UI) simples, funcional e de rápido desenvolvimento.
 
## Persona
 
O chatbot é voltado para síndicos e gestores prediais, pois são os responsáveis pela administração dos eletropostos e necessitam de informações rápidas para tomada de decisão.
 
Proposta do Chatbot
(seu conteúdo continua igual)
 
##  Proposta do Chatbot
O chatbot será focado na solução **EV ChargeOps**, servindo como um assistente operacional para **Síndicos e Gestores Prediais**.
Ele permitirá:
1. Consultar o status de ocupação e disponibilidade das estações em tempo real.
2. Gerar resumos detalhados de consumo por unidade/apartamento para rateio de custos.
3. Oferecer suporte técnico de primeiro nível para erros comuns e manutenção preventiva nos carregadores GoodWe.
 
##  Fluxograma de Funcionamento
O fluxo operacional compreende a entrada da dúvida do gestor, a filtragem de dados via Pandas, o processamento lógico pelo Gemini e a entrega da solução contextualizada.
 <img width="681" height="726" alt="fluxograma" src="https://github.com/user-attachments/assets/bb57a4cf-b441-461c-a7f6-bc4206538ac1" />
 
##  Contexto-Base (System Prompt)
"Você é o GoodWe ChargeOps Assistant, um assistente especializado na gestão de eletropostos em condomínios.
Seu objetivo é auxiliar síndicos e gestores prediais na tomada de decisão, fornecendo informações precisas sobre consumo de energia, uso das estações, faturamento e suporte técnico básico.
 
Você deve:
- Utilizar os dados de logs fornecidos (CSV/JSON) para responder perguntas quantitativas
- Realizar cálculos como soma de consumo (kWh) e agrupamento por unidade
- Interpretar erros técnicos com base em padrões conhecidos
- Fornecer respostas claras, diretas e acionáveis
 
Nunca invente dados. Caso a informação não esteja disponível, informe claramente ao usuário."
 
## Modelo de Teste (Perguntas e Respostas Esperadas)
 
1. **Pergunta:** "Qual o consumo total do carregador 01 este mês?"
   **Resposta esperada:** O consumo total do carregador 01 no mês atual é de 245 kWh, considerando os dados registrados entre o início e o final do período analisado.
 
2. **Pergunta:** "O apartamento 102 realizou alguma recarga hoje?"
   **Resposta esperada:** Sim, o apartamento 102 realizou uma recarga hoje. A última sessão foi registrada às 18:45, com duração de 1h20.
 
3. **Pergunta:** "O que significa a luz vermelha piscando no carregador?"
   **Resposta esperada:** A luz vermelha piscando indica uma falha no sistema. Recomenda-se verificar o aterramento do equipamento e reiniciar o carregador. Caso o problema persista, é necessário acionar o suporte técnico.
 
4. **Pergunta:** "Como faço para cadastrar um novo morador no sistema?"
   **Resposta esperada:** Para cadastrar um novo morador, acesse o sistema de gestão do EV ChargeOps, vá até a seção de usuários, selecione "Adicionar novo usuário" e registre os dados do morador juntamente com a tag de acesso ao carregador.
 
5. **Pergunta:** "Gere um relatório de faturamento para o Bloco A."
   **Resposta esperada:** O faturamento total do Bloco A no período analisado é de R$ 1.250,00, considerando o consumo individual de todas as unidades e a tarifa de energia aplicada.
