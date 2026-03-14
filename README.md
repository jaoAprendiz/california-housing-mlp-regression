# 🏡 Predição de Preços de Imóveis na Califórnia com Redes Neurais (MLP)

Um projeto prático de Machine Learning focado na estimativa do valor mediano de imóveis no estado da Califórnia utilizando Redes Neurais Artificiais (Perceptron de Múltiplas Camadas - MLP). 

## 🎓 Créditos e Contexto Acadêmico
[cite_start]Este case foi desenvolvido como parte do módulo de Inteligência Artificial e Machine Learning (Generative AI for Engineering) do curso de Engenharia de Software da FIAP[cite: 1, 2]. 
A estrutura base do código e a fundamentação teórica deste projeto foram ministradas e disponibilizadas pelo **Prof. [cite_start]Dr. Francisco Elânio**. Este repositório representa a minha implementação, organização e análise em cima desse material rico para compor meu portfólio prático.

---

## 🎯 Objetivo do Projeto
O objetivo central foi treinar um modelo de regressão capaz de prever com precisão os preços medianos das casas utilizando variáveis numéricas locais. Inicialmente, o modelo puro apresentou uma taxa de perda (loss) muito alta durante o treinamento. Para otimizar a performance e garantir a convergência da rede neural, aplicamos técnicas estatísticas de pré-processamento, o que reduziu drasticamente os erros de previsão.

## 🛠️ Tecnologias e Ferramentas
O projeto foi construído 100% em **Python**, aplicando algumas das melhores bibliotecas do ecossistema de dados:
* **Pandas:** Leitura, manipulação e estruturação do dataset.
* **Scikit-Learn:** Construção do modelo `MLPRegressor`, separação de dados (treino/teste) e aplicação do `StandardScaler`.
* **Plotly Express & Folium:** Renderização de mapas interativos para visualização geoespacial avançada, incluindo marcadores e distribuição de renda e população.
* **Matplotlib:** Geração de gráficos analíticos, como a curva de loss e o gráfico de dispersão (Valor Real vs. Valor Previsto).

## 🗺️ Análise Exploratória (EDA)
Durante a exploração dos dados, mapeamos os imóveis para entender a dinâmica de preços geograficamente. Através das bibliotecas de visualização, cruzamos a latitude e longitude com o valor mediano, renda e população, criando mapas interativos que facilitam a identificação das áreas mais valorizadas do estado.

## ⚙️ Modelagem e o Poder da Normalização
A arquitetura da rede neural foi configurada com múltiplas camadas ocultas e limite de iterações. No entanto, o grande salto de qualidade do modelo ocorreu após a etapa de pré-tratamento. 

Aplicamos o `StandardScaler` para normalizar tanto os dados de entrada quanto a variável de saída. Esse processo transformou as variáveis para terem média igual a 0 e desvio padrão igual a 1, padronizando a escala e facilitando o aprendizado da rede neural.

### 📈 Comparativo de Performance
O desempenho do modelo foi validado utilizando duas métricas principais: **R²** (Coeficiente de Determinação) e **MAPE** (Erro Percentual Absoluto Médio):

| Métrica | Antes da Normalização | Depois da Normalização |
| :--- | :--- | :--- |
| **R²** | 0.32 | 0.85 (Treino) / 0.78 (Teste) |
| **MAPE** | 47% | 18% |

*A aplicação da normalização fez o erro percentual médio cair de 47% para apenas 18%, estabilizando a curva de loss e provando a eficácia do pré-tratamento de dados em modelos de Deep Learning.*

## 🚀 Como Executar o Projeto Localmente
1. Clone este repositório para a sua máquina.
2. Certifique-se de ter o Python instalado.
3. Instale as dependências executando: `pip install -r requirements.txt`
4. Abra o notebook principal em sua IDE favorita (como VS Code ou Jupyter) e execute as células.

---
**Desenvolvido por João Victor Soave**
