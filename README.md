# 📊 Tech Challenge - Fase 1 | Data Analytics (FIAP Pós-Tech)
## Diagnóstico Estratégico e Operacional: E-commerce Olist (2017–2018)

Este repositório contém o pipeline analítico, tratamento e limpeza de dados, enriquecimento com benchmark de mercado, geração de métricas de negócio e exportação de visualizações executivas desenvolvidas para a avaliação da Fase 1 da Pós-Graduação em Data Analytics.

---

### 📌 Entregáveis Oficiais
* **Repositório GitHub:** `https://github.com/diegoolsilva/analise_olist`
* **Apresentação Executiva (Google Slides):** `https://docs.google.com/presentation/d/1ds7gheDAoapEgzYRsnGeAE47jLrAnDOCg9STFbRxreQ/edit?usp=sharing`
* **Vídeo de Apresentação Executiva (até 5 min):** [COLE_AQUI_O_LINK_DO_VÍDEO]

---

### 🎯 Contexto de Negócio & Escopo Analítico
A partir da base transacional pública da Olist (~100 mil pedidos), realizou-se uma auditoria analítica voltada a comitês executivos e investidores, estruturada em três trilhas centrais enriquecidas com dados macroeconômicos de mercado:

1. **Tração Comercial & Motores de Crescimento**
2. **Eficiência Logística, SLAs e Satisfação do Cliente (NPS)**
3. **Dinâmica Financeira e Alavancagem por Crédito**

#### Governança Temporal & Metodologia
* **Auditoria Amostral (4T2016):** Identificou-se ausência de registros em novembro de 2016 e dados esparsos de homologação. O período foi excluído por governança estatística.
* **Recorte Analítico Oficial:** Janeiro de 2017 a Agosto de 2018 (20 meses contínuos).
* **Critério Contábil:** Análises focadas estritamente em pedidos liquidados com status entregue (`status == 'delivered'`).

---

### 📈 Principais Descobertas e Indicadores (KPIs)

#### 1. Tração Comercial & Benchmark de Mercado
* **Escala Acelerada:** A receita mensal saltou de R$ 120,3 mil (Jan/17) para R$ 1,00 milhão (Ago/18), representando um **crescimento acumulado de +729%** (multiplicação de **8,3x**).
* **Crescimento Anual Médio (YoY):** **+146,8% a.a.**
* **Benchmark Nacional e Global:** O ritmo de expansão da Olist superou amplamente a média do comércio eletrônico brasileiro (**+12,0% a.a.** segundo dados dos relatórios *Webshoppers / Ebit Nielsen*) e do e-commerce mundial (**~23% a 24% a.a.** segundo estimativas da *eMarketer / Insider Intelligence*), comprovando captura acelerada de *market share*.
* **Comportamento da Cesta:** Ticket médio estável oscilando entre **R$ 124 e R$ 149**, evidenciando que a tração decorreu exclusivamente da aquisição de clientes e volume de pedidos.

#### 2. Concentração de Portfólio (Regra de Pareto)
* **Regra 80/20:** As primeiras **7 categorias líderes** respondem por **~50,5%** de todo o faturamento da plataforma (*Beleza e Saúde* e *Relógios & Presentes* no topo).
* **Concentração Regional:** O **Top 5 estados** concentra **73,9%** da receita, com o estado de São Paulo isolado em **38,3%**.

#### 3. Logística & Nível de Serviço (SLA)
* **Cumprimento de Prazos:** **92,1%** das entregas realizadas dentro da data limite estimada, com mediana nacional de **10,2 dias corridos**.
* **Destruição de NPS por Atraso:** Em pedidos entregues no prazo, as avaliações com Nota 1 representam apenas **8,4%** (satisfação plena de notas 4 e 5 supera 80%). Quando ocorre atraso na entrega, a proporção de avaliações Nota 1 salta para **46,9%** (aumento relativo superior a 5,5x).

#### 4. Meios de Pagamento & Financiamento
* **Hegemonia do Cartão:** O cartão de crédito representa **78,5% do faturamento** (ticket médio de **R$ 162,24**), seguido pelo Boleto Bancário (**18,0%**).
* **Alavanca de Ticket por Parcelamento:** O parcelamento atua diretamente no destravamento de carrinhos de maior valor, registrando um aumento de cerca de **40% no ticket médio** a partir de 2 a 3 prestações.

---

### 🛠️ Estrutura do Repositório

```text
analise_olist/
│
├── graficos/
│   ├── 01_evolucao_receita_pedidos.png
│   ├── 02_evolucao_ticket_medio.png
│   ├── 03_pareto_categorias.png
│   ├── 04_prazo_x_satisfacao.png
│   ├── 05_top_5_estados.png
│   └── 06_ticket_medio_parcelas_cartao.png
├── analise_executiva_olist.ipynb
├── .gitignore
├── requirements.txt
└── README.md