🏦 Previsão de Score de Crédito com Machine Learning

Este projeto resolve um problema real do setor bancário: classificar automaticamente o score de crédito de clientes (Ruim, Ok ou Bom) com base em suas informações financeiras e de comportamento. Utilizei técnicas de Machine Learning para treinar e comparar modelos, alcançando uma acurácia de 82,27% com o melhor algoritmo.

🎯 Contexto do Problema

Um banco precisa analisar milhares de clientes diariamente. Manualmente, isso é inviável. O objetivo é construir um modelo preditivo que leia as características do cliente e retorne seu nível de risco (Poor, Standard, Good) de forma rápida e precisa.

🛠️ Tecnologias Utilizadas

Python 3.8+
Pandas & NumPy (Manipulação e análise de dados)
Scikit-learn (Pré-processamento e Modelagem)

LabelEncoder (Transformação de variáveis categóricas)
RandomForestClassifier & KNeighborsClassifier (Modelos de Machine Learning)
train_test_split (Divisão de dados)
accuracy_score (Métrica de avaliação)
📂 Estrutura do Projeto / Passo a Passo

Análise Inicial dos Dados: Importei a base (clientes.csv) com 100.000 registros e 25 colunas, entendendo os tipos de dados e distribuições.
Pré-processamento (Feature Engineering):

Como a IA só entende números, utilizei o LabelEncoder para transformar colunas categóricas (profissao, mix_credito, comportamento_pagamento) em valores numéricos.
Eliminei colunas irrelevantes para a predição, como id_cliente e a própria score_credito (que é o nosso alvo).
Divisão dos Dados: Separei 70% dos dados para treino e 30% para teste.
Treinamento dos Modelos: Treinei dois algoritmos distintos:

Random Forest (Árvore de Decisão em Conjunto)
KNN (K-Vizinhos Mais Próximos)
Avaliação e Escolha: Comparei a acurácia de ambos.

✅ Random Forest: 82.27% (Modelo Vencedor)
❌ KNN: 73.72%
Previsão para Novos Clientes: Utilizei o modelo treinado (Random Forest) para prever o score de uma base de novos clientes (novos_clientes.csv), aplicando o mesmo pré-processamento.
📊 Resultados e Insights

O Random Forest se mostrou muito mais eficaz para esse tipo de dado tabular, provavelmente devido à sua capacidade de lidar com relações não lineares e interações entre features.
O modelo final é capaz de classificar novos clientes em segundos, otimizando a análise de risco do banco.
