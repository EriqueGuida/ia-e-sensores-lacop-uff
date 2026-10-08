# 03 — Reconhecimento de Atividade Humana

Projeto de Machine Learning aplicado à classificação de atividades humanas a partir de dados de acelerômetros.

## Objetivo

Classificar registros de movimento em três categorias:

* **Alta Intensidade** — Walking, Running e Cycling
* **Atividade Leve** — Standing e Shuffling
* **Sedentário** — Sitting e Lying

O modelo utiliza leituras dos acelerômetros posicionados nas regiões **lombar (back)** e **coxa (thigh)**.

## Abordagem

* Dataset HARTH, utilizando o participante `S022` e posteriormente um grupo de participantes.
* Seleção de seis variáveis dos acelerômetros:
  `back_x`, `back_y`, `back_z`, `thigh_x`, `thigh_y`, `thigh_z`.
* Classificação supervisionada.
* Divisão dos dados em treino e teste com estratificação.
* Modelo utilizado: **Random Forest Classifier**.
* Avaliação por acurácia, relatório de classificação e matriz de confusão.

## Resultados

| Experimento            |  Acurácia | Baseline |
| ---------------------- | --------: | -------: |
| Participante S022      | **95,8%** |    56,7% |
| Grupo de participantes | **97,2%** |    33,3% |

No experimento com o grupo de participantes, o modelo apresentou **63,9 pontos percentuais acima do baseline**.

A matriz de confusão indica que a maior parte das classificações ficou concentrada na diagonal, representando previsões corretas.

## Tecnologias

* Python
* Pandas
* NumPy
* Scikit-learn
* Random Forest
* Jupyter Notebook / Google Colab

## Estrutura

```text
03-reconhecimento-de-atividade/
├── README.md
├── reconhecimento_atividade_harth.ipynb
└── resultados/
```

## Limitações

* O experimento utiliza divisão aleatória entre treino e teste, o que pode produzir uma estimativa otimista quando existem registros temporalmente próximos ou do mesmo participante nos dois conjuntos.
* A generalização para novos indivíduos deve ser avaliada com uma estratégia de validação por participante.
* O mapeamento dos rótulos do dataset deve ser validado antes da publicação dos resultados definitivos.

## Próximos passos

* Validar o mapeamento dos rótulos do HARTH.
* Reexecutar os experimentos após a correção.
* Avaliar generalização utilizando participantes não presentes no treinamento.
* Comparar Random Forest com outros classificadores.
* Explorar características temporais dos sinais dos acelerômetros.

## O que este projeto demonstra

* Preparação de dados de sensores.
* Engenharia e seleção de features.
* Classificação supervisionada.
* Avaliação de modelos de Machine Learning.
* Interpretação de matriz de confusão.
* Aplicação de IA a dados de sensores e reconhecimento de padrões.
