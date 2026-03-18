# 📊 Teste A/B — Sistema de Recomendação

## 📌 Contexto

Uma loja online internacional realizou um teste A/B para avaliar o impacto de um novo sistema de recomendação de produtos no comportamento dos usuários.

O experimento comparou dois grupos:

* **Grupo A (controle):** sistema atual
* **Grupo B (teste):** novo sistema de recomendação

O objetivo foi verificar se o novo sistema aumentaria a conversão dos usuários ao longo do funil de compras.

---

## 🎯 Objetivo

Avaliar se o novo sistema de recomendação melhora a conversão dos usuários em cada etapa do funil:

**login → product_page → product_cart → purchase**

A hipótese do negócio era um aumento de **pelo menos 10% nas conversões**.

---

## 🧪 Metodologia

* Análise exploratória dos dados (EDA)
* Limpeza e preparação dos dados
* Validação da qualidade do experimento
* Construção do funil de conversão
* Aplicação de **teste estatístico (teste Z para proporções)**

**Nível de significância:** 5% (α = 0.05)

---

## ⚠️ Validação do experimento

Antes da análise, foram identificados pontos importantes:

* Desbalanceamento entre grupos:

  * Grupo A: 74,7%
  * Grupo B: 25,3%
* Remoção de usuários em múltiplos testes
* Foco apenas em usuários da região EU
* Queda de eventos nos últimos dias do experimento

Esses fatores podem impactar a confiabilidade dos resultados.

---

## 📊 Principais insights

* O novo sistema **reduziu a conversão na etapa de visualização de produtos (product_page)**
* Não houve diferença estatisticamente significativa nas etapas:

  * login
  * product_cart
  * purchase
* O funil apresentou comportamento esperado (queda progressiva de usuários)
* Pequena inconsistência: compras sem registro de adição ao carrinho

---

## 📈 Resultado do teste estatístico

* Apenas a etapa **product_page** apresentou diferença significativa (p < 0.05)
* O grupo de teste (B) teve desempenho **inferior** ao grupo controle (A)
* Nas demais etapas, **não houve evidência estatística de diferença**

---

## 🧠 Conclusão

O novo sistema de recomendação **não melhorou a conversão dos usuários**.

Além disso, apresentou desempenho inferior na etapa inicial do funil.

📌 **Recomendação:**
Não implementar o novo sistema neste momento.

---

## ⚠️ Limitações

* Desbalanceamento entre os grupos
* Possível viés na coleta de dados
* Redução de eventos no final do experimento
* Múltiplas comparações estatísticas (risco de erro tipo I)

---

## 🛠️ Tecnologias utilizadas

* Python (Pandas, NumPy)
* Statsmodels
* Matplotlib / Seaborn

---

## 📂 Estrutura do projeto

```bash
├── notebooks/
│   └── ab_test_analysis.ipynb
├── data/
│   ├── ab_project_marketing_events_us.csv
│   ├── final_ab_new_users_upd_us.csv
│   ├── final_ab_events_upd_us.csv
│   └── final_ab_participants_upd_us.csv
└── README.md
```

---

## 🚀 Como executar

1. Clone o repositório:

```bash
git clone https://github.com/seu-usuario/Recommender-system-ab-test.git
```

2. Instale as dependências:

```bash
pip install -r requirements.txt
```

3. Execute o notebook:

```bash
jupyter notebook
```

---

## 💡 Sobre o projeto

Este projeto simula um cenário real de negócio, onde decisões de produto são baseadas em experimentação e análise estatística.

O foco não é apenas a análise técnica, mas a **tomada de decisão orientada por dados**.
