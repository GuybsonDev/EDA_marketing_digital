# Projeto Parceria Semantix — EDA de Marketing Digital

Este projeto realiza uma Análise Exploratória de Dados (EDA) sobre campanhas de marketing digital, com foco em eficiência de canais e tipos de campanha. O notebook principal é `analise_marketing.ipynb` e os dados de entrada estão em `digital_marketing_campaign_dataset_ptbr.csv`.

Link do dashboard para acompanhar os insights fornecidos: https://lookerstudio.google.com/reporting/d04e0452-ba6e-450f-8965-bffd18a477c9/page/6zWmF

## Coleta de dados

- **Fonte:** dataset público do Kaggle (predict conversion in digital marketing).
- **Link:** https://www.kaggle.com/datasets/rabieelkharoua/predict-conversion-in-digital-marketing-dataset
- **Arquivo utilizado no projeto:** `digital_marketing_campaign_dataset_ptbr.csv` (formato pt-BR, separador `;`, decimal `,`).
- **Contexto dos dados:** métricas de campanhas digitais por canal e tipo de campanha, incluindo gasto, CTR, CVR, visitas e conversões.
- **Observação:** dados públicos, não confidenciais, adequados para análises educacionais e de marketing.

## Modelagem

Nesta etapa, a “modelagem” refere-se à preparação analítica e criação de métricas derivadas para suportar a EDA e o dashboard.

- **Limpeza e consistência:**
  - Verificação de nulos e duplicados.
  - Tipos numéricos padronizados.
- **Métricas derivadas:**
  - **CPA** = `AdSpend / Conversion`
  - **CPC** = `AdSpend / WebsiteVisits`
  - **Engajamento de site** = `PagesPerVisit * TimeOnSite`
- **Agregações principais:**
  - Por **CampaignChannel** (canal)
  - Por **CampaignType** (tipo de campanha)
- **Limitações da modelagem:**
  - Não há coluna temporal (impossível analisar tendências).
  - Não há coluna de receita (ROAS não pode ser calculado).

## Conclusões

Principais conclusões consistentes com a análise e o dashboard:

- **Gargalo principal está no custo e alocação de budget**, não em conversão.
- **Email e Referral** apresentam boa relação custo x conversão.
- **PPC**, apesar de CPC alto, tende a ser eficiente em conversão no fim do funil (melhor CPA em alguns cenários).
- **Social Media** é mais forte no topo de funil e precisa de otimização para conversão.
- Canais devem **atuar de forma complementar** no funil, não competindo entre si.

## Como executar

1) Instale dependências:
```
pip install -r requirements.txt
```

2) Abra o notebook:
```
jupyter notebook analise_marketing.ipynb
```

---

