# 02 — Previsão do Consumo de Energia

Projeto de **Machine Learning aplicado à análise e previsão do consumo de energia**, desenvolvido no Workshop de Inteligência Artificial e Sensores do LACOP — Universidade Federal Fluminense (UFF).

O objetivo é prever o **consumo de energia elétrica por hora**, utilizando características temporais, ambientais e de ocupação do prédio.

## Objetivo

Desenvolver um modelo de regressão capaz de estimar a variável `consumo_kwh` a partir de informações disponíveis para cada período.

As principais variáveis utilizadas foram:

* Hora
* Fim de semana
* Feriado
* Temperatura externa
* Umidade externa
* Ocupação do prédio
* Tarifa de ponta
* Dia da semana

## Abordagem

O problema foi tratado como uma tarefa de **regressão supervisionada**.

Além da previsão do consumo, o projeto também analisa a diferença de consumo médio entre **dias úteis e dias não úteis**, buscando identificar padrões de utilização da energia.

O desempenho do modelo foi comparado com um **baseline**, que utiliza a média da variável-alvo como previsão.

A métrica utilizada foi o **erro médio absoluto (MAE)**, em que valores menores indicam previsões mais próximas dos valores reais.

## Resultados

| Modelo                     |           MAE |
| -------------------------- | ------------: |
| Baseline — média da base   | **16,15 kWh** |
| Modelo de Machine Learning |  **2,06 kWh** |

O modelo apresentou uma redução de aproximadamente **87% no erro médio** em relação ao baseline.

Esse resultado indica que as variáveis temporais, ambientais e de ocupação utilizadas no experimento possuem relação relevante com o consumo observado.

### Previsões × valores reais

O projeto também apresenta uma comparação entre os valores reais de consumo e as previsões do modelo. Quanto mais próximas as previsões estiverem dos valores reais, melhor o desempenho da regressão.

## Tecnologias

* Python
* Pandas
* Scikit-learn
* Jupyter Notebook
* Machine Learning
* Regressão

## Estrutura

```text
02-consumo-de-energia/
├── README.md
├── previsao_consumo_energia.ipynb
└── resultados/
    └── ...
```

## Limitações

O experimento utiliza dados com componente temporal. Uma avaliação baseada em uma separação cronológica entre treinamento e teste seria uma evolução importante para verificar a capacidade do modelo de generalizar para períodos futuros.

Além disso, os resultados apresentados correspondem ao experimento realizado no workshop e devem ser validados em novos períodos de coleta antes de uma utilização operacional.

## Próximos passos

* Avaliar o modelo utilizando divisão temporal dos dados;
* Explorar variáveis derivadas de horário e sazonalidade;
* Comparar diferentes algoritmos de regressão;
* Avaliar o modelo em períodos de consumo não utilizados no treinamento;
* Investigar estratégias para previsão e monitoramento do consumo energético.

## O que este projeto demonstra

* Análise de dados de consumo energético;
* Preparação de variáveis para Machine Learning;
* Formulação de um problema de regressão;
* Avaliação utilizando MAE;
* Comparação entre modelo e baseline;
* Análise de padrões de consumo;
* Interpretação de resultados e identificação de limitações.
