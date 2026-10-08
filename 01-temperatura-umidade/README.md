# 01 — Previsão da Temperatura da Sala em 1 Hora

Projeto de **Machine Learning aplicado a sensores ambientais**, desenvolvido no Workshop de Inteligência Artificial e Sensores do LACOP — Universidade Federal Fluminense (UFF).

O objetivo é prever a **temperatura da sala uma hora à frente** a partir de informações ambientais e de ocupação.

## Objetivo

Desenvolver um modelo de regressão capaz de estimar a variável `temp_daqui_1h` utilizando dados coletados no ambiente.

As variáveis utilizadas como entrada foram:

* Temperatura atual (`temperatura_c`)
* Umidade relativa (`umidade_pct`)
* Luminosidade (`luminosidade_lux`)
* Estado do ar-condicionado (`ar_condicionado`)
* Número estimado de pessoas (`pessoas_estimadas`)
* Identificação da sala (`sala_Sala_Aula`)

## Abordagem

O projeto utiliza uma abordagem de **regressão supervisionada**, na qual o modelo aprende a relacionar as condições observadas no ambiente com a temperatura esperada para a próxima hora.

O desempenho foi comparado com um **baseline**, que utiliza a média da variável-alvo como previsão.

A métrica utilizada foi o **erro médio absoluto (MAE)**, em que valores menores representam previsões mais próximas dos valores reais.

## Resultados

| Modelo                     |         MAE |
| -------------------------- | ----------: |
| Baseline — média da base   | **3,18 °C** |
| Modelo de Machine Learning | **1,25 °C** |

O modelo apresentou uma redução de aproximadamente **61% no erro médio** em relação ao baseline.

Isso indica que as variáveis utilizadas fornecem informações relevantes para a previsão da temperatura futura.

### Previsões × valores reais

O relatório apresenta a comparação entre os valores previstos pelo modelo e os valores reais observados. Quanto mais próximos os pontos estiverem da linha de previsão perfeita, melhor o desempenho da regressão.

## Tecnologias

* Python
* Pandas
* Scikit-learn
* Jupyter Notebook
* Machine Learning
* Regressão

## Estrutura

```text
01-temperatura-e-umidade/
├── README.md
├── previsao_temperatura.ipynb
└── resultados/
    └── ...
```

O notebook contém as etapas de análise e desenvolvimento do modelo, enquanto os resultados são apresentados separadamente para facilitar a consulta.

## Limitações

O resultado apresentado representa o desempenho obtido no experimento realizado no workshop. Por se tratar de dados com componente temporal, uma avaliação utilizando uma separação temporal entre treinamento e teste seria uma evolução importante para verificar melhor a capacidade de generalização do modelo para períodos futuros.

## Próximos passos

* Avaliar o modelo utilizando uma divisão temporal dos dados;
* Explorar novas variáveis derivadas dos sensores;
* Comparar diferentes algoritmos de regressão;
* Avaliar o modelo em dados coletados em novos períodos.

## O que este projeto demonstra

* Preparação e utilização de dados de sensores;
* Formulação de um problema de regressão;
* Treinamento e avaliação de modelos de Machine Learning;
* Comparação de modelo com baseline;
* Interpretação de métricas de erro;
* Identificação de limitações e possibilidades de melhoria.
