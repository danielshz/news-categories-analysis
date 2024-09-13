# 📰 Análise textual de resumos de notícias

Este repositório contém o código e o relatório final do projeto "Análise Textual de Resumo de Notícias", realizado como parte da disciplina **Introdução ao Aprendizado de Máquina (2024/1)** no Instituto de Computação da Universidade Federal do Rio de Janeiro <a href="https://ufrj.br/" target="blank">(UFRJ)</a>.

## 🎯 Objetivo

O projeto visa a classificação de resumos de notícias de acordo com seus temas, utilizando técnicas de vetorização de textos e algoritmos de aprendizado de máquina. A partir disso, foi realizada a comparação entre os modelos de **Regressão Logística** e **Floresta Aleatória** para determinar qual algoritmo apresenta melhor desempenho na tarefa de classificação.

## 🗄️ Base de Dados

Os dados utilizados foram extraídos do [News Category Dataset](https://www.kaggle.com/rmisra/news-category-dataset), que contém mais de 200 mil manchetes e resumos de notícias publicadas entre 2012 e 2022 no [HuffPost](https://www.huffpost.com/).

Os atributos principais utilizados no projeto foram:

- **headline**: título da notícia
- **short description**: resumo da notícia
- **category**: categoria da notícia (variável alvo)

## 🛠️ Pré-processamento

As etapas de pré-processamento incluem:

1. **Tokenização**: Segmentação do texto em palavras.
2. **Remoção de caracteres não-alfabéticos**: Exclusão de números e pontuações.
3. **Remoção de stop-words**: Exclusão de palavras irrelevantes (como artigos e pronomes).
4. **Stemming**: Redução das palavras às suas raízes.
5. **Vetorização**: Conversão dos textos em vetores utilizando a técnica de **TF-IDF**.

## 📊 Modelos Utilizados

1. **Regressão Logística**: Um modelo linear simples e eficiente para a classificação multiclasse.
2. **Floresta Aleatória**: Um ensemble de árvores de decisão, conhecido pela sua robustez e capacidade de interpretar a importância dos atributos.

Ambos os modelos foram otimizados utilizando a técnica de **Grid Search** para encontrar os melhores hiperparâmetros.

## 📈 Resultados

- **Regressão Logística**: 
  - Acurácia de teste: 92%
  - F1-Score (Macro): 0.87
  - Melhor desempenho geral para a tarefa de classificação.

- **Floresta Aleatória**:
  - Acurácia de teste: 84%
  - F1-Score (Macro): 0.83
  - Apresentou maior interpretabilidade, mas desempenho inferior à regressão logística.

## 🏁 Conclusão

A **Regressão Logística** demonstrou ser um modelo eficiente para a tarefa de classificação de textos, apresentando uma acurácia maior em comparação à Floresta Aleatória. Além disso, o projeto evidenciou a importância do pré-processamento dos dados e da escolha adequada de modelos de aprendizado para tarefas de classificação textual.

## 🔗 Referências

Avikumart (2022). [nlp] news articles classif (wordembeddings&rnn). Acessado em: 2024-06-13.

Heng (2018). News category classifier (val acc 0.65). Acessado em: 2024-06-13.

Manning, C. D. (2008). Introduction to information retrieval. Syngress Publishing,. Capítulos 1, 2, 6 e 8.

Misra, R. (2022). News category dataset. arXiv preprint arXiv:2209.11429.

Misra, R. and Grover, J. (2021). Sculpting Data for ML: The first act of Machine Learning.
