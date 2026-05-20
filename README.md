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
* **IA/LLM:** OpenAI
  * *Justificativa:* Escolhido pela alta capacidade de interpretar linguagem natural e gerar respostas contextualizadas com base em dados operacionais de contexto e integração nativa com ferramentas de análise.
* **Análise de Dados:** Pandas
  * *Justificativa:* Biblioteca essencial para simular a leitura de bancos de dados de consumo e gerar relatórios precisos para o síndico.
* **Interface:** Gradio
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
Seu objetivo é auxiliar síndicos e gestores prediais na tomada de decisão, fornecendo informações precisas sobre suporte técnico básico.
 
Você deve:
- Utilizar os dados de logs fornecidos (CSV/JSON) para responder perguntas quantitativas
- Realizar cálculos como soma de consumo (kWh) e agrupamento por unidade
- Interpretar erros técnicos com base em padrões conhecidos
- Fornecer respostas claras, diretas e acionáveis
 
Nunca invente dados. Caso a informação não esteja disponível, informe claramente ao usuário."
 
## Modelo de Teste (Perguntas e Respostas Esperadas)
 
1. **Pergunta:** "Como fazer Download e Instalação do Aplicativo?"

   **Resposta esperada:** Método 1: Pesquise SEMS Portal no Google Play (Android) ou na App Store (iOS) para instalar; Método 2 Digitalize o código QR abaixo para instalar. 
 
2. **Pergunta:** "Como Desmantar o carregador?"

   **Resposta esperada:** Etapa 1: Desconecte todos os cabos, incluindo cabos CA e de comunicação.
                          Etapa 2: Remova o carregador da placa de montagem.
                          Etapa 3: Remova a placa de montagem.
                          Etapa 4: Guarde o carregador adequadamente. 
Se o carregador precisar ser usado posteriormente, certifique-se de que as condições de armazenamento atendam aos requisito
 
3. **Pergunta:** "Quais são as Funcionalidades?"

   **Resposta esperada:**  Controle dinâmico de carga e Garantir potência mínima de carregamento
 
4. **Pergunta:** "Como Desligar o carregador?"

   **Resposta esperada:** Desligue o carregador antes das operações e manutenção. Caso contrário, o carregador pode ser danificado ou podem ocorrer choques elétricos.Desconecte o RCBO entre o carregador e a rede/o inversor
 
5. **Pergunta:** "Sobre a Conexão elétrica, quais são as precauções de segurança?"

   **Resposta esperada:** Siga sempre as normas e leis locais para instalações elétricas.
Desligue a energia antes de trabalhar para evitar choque elétrico.
Organize os cabos corretamente (sem cruzar ou emaranhar) e deixe folga para evitar tensão.
Faça conexões bem firmes: o fio condutor deve ter contato total com o terminal.
Use equipamentos de proteção (luvas, botas, etc.) e conte com profissionais qualificados.
Utilize cabos adequados (evite alumínio e cobre sólido).
Conecte os cabos nos terminais corretos (L1, L2, L3, N, PE).
Garanta que nenhum fio fique exposto e que tudo esteja bem fixado para evitar superaquecimento e danos.

## Avaliação Qualitativa

**Pergunta 1:** Adequada.

**Pergunta 2:** Adequada.

**Pergunta 3:** Inadequada.

**Pergunta 4:** Adequada

**Pergunta 5:** Adequada
