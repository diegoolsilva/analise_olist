# 📊 Tech Challenge - Fase 1 | Data Analytics (FIAP Pós-Tech)
## Diagnóstico Estratégico e Operacional: E-commerce Olist (2017–2018)

Este repositório contém o pipeline analítico, tratamento e limpeza de dados, geração de indicadores de negócio e exportação de visualizações executivas desenvolvidas para a avaliação da Fase 1 da Pós-Graduação em Data Analytics.

---

### 📌 Entregáveis Oficiais
* **Apresentação Executiva (Google Slides):** [COLE_AQUI_O_LINK_DO_GOOGLE_SLIDES]
* **Vídeo de Apresentação Executiva:** [COLE_AQUI_O_LINK_DO_VÍDEO]

---

### 🎯 Contexto de Negócio & Escopo Analítico
A partir da base transacional pública da Olist (~100 mil pedidos), realizou-se uma auditoria analítica voltada a comitês executivos e investidores, estruturada em três trilhas centrais:

1. **Tração Comercial & Motores de Crescimento**
2. **Eficiência Logística, SLAs e Satisfação do Cliente (NPS)**
3. **Dinâmica Financeira e Alavancagem por Crédito**

#### Governança Temporal & Metodologia
* **Auditoria de Dados (4T2016):** Identificou-se ausência completa de registos em novembro de 2016 e dados esparsos de homologação. O período foi excluído por governança amostral.
* **Recorte Oficial:** Janeiro de 2017 a Agosto de 2018 (20 meses contínuos).
* **Critério Contábil:** Análises focadas estritamente em pedidos com status final entregue (`status == 'delivered'`).

---

### 📈 Principais Descobertas e Indicadores (KPIs)

* **Crescimento & Escala:** Faturamento impulsionado primariamente pelo volume de novos pedidos, com ticket médio estável oscilando entre **R$ 124 e R$ 149**.
* **Concentração de Mercado:** O **Top 10 categorias** responde por **63,3% da receita** (*Beleza e Saúde* na liderança). Os **Top 5 estados** concentram **73,9%**, com São Paulo isolado em **38,3%**.
* **Nível de Serviço (SLA):** **92,1%** dos pedidos entregues dentro do prazo prometido, com mediana nacional de **10,2 dias corridos**.
* **Impacto do Atraso no NPS:** Em pedidos no prazo, avaliações com Nota 1 representam apenas **8,4%** (mais de 80% de satisfação plena em Notas 4 e 5). Quando ocorre atraso, a Nota 1 salta para **46,9%** (aumento relativo superior a 5,5x).
* **Meios de Pagamento:** Hegemonia absoluta do **Cartão de Crédito** (**78,5% da receita** e tíquete médio de **R$ 162,24**), seguido pelo Boleto Bancário (**18,0%**).
* **Alavanca do Parcelamento:** O parcelamento atua diretamente no aumento da cesta de compras, registando um salto de cerca de **40% no tíquete médio** a partir de 2 a 3 prestações.

---

### 🛠️ Estrutura de Arquivos
```text
├── graficos_executivos/         # Gráficos em alta resolução (300 DPI)
│   ├── 01_evolucao_ticket_medio.png
│   ├── 02_top_10_categorias.png
│   ├── 03_top_5_estados.png
│   ├── 04_impacto_logistica_satisfacao.png
│   └── 05_parcelas_vs_ticket_medio.png
├── notebooks/                   # Pipeline analítico reproduzível (.ipynb)
├── .gitignore                   # Filtro para arquivos pesados (.csv) e ambiente local
├── requirements.txt             # Dependências e bibliotecas do projeto
└── README.md                    # Sumário executivo e documentação