# Notebooks

Esta pasta contém os notebooks utilizados no desenvolvimento dos experimentos do trabalho:

**Avaliação da qualidade de dormentes de concreto baseado em visão computacional**

O notebook principal implementa o pipeline completo de pré-processamento, aumento de dados, treinamento, avaliação e comparação dos modelos utilizados no estudo.

## Notebook disponível

| Arquivo | Descrição |
|---|---|
| `01_pipeline_classificacao_dormentes.ipynb` | Pipeline completo do experimento, incluindo pré-processamento das imagens, data augmentation, treinamento das CNNs, treinamento dos modelos clássicos e geração dos resultados comparativos. |

## Estrutura geral do notebook

O notebook está organizado nas seguintes etapas:

1. **Configuração inicial**
   - Montagem do Google Drive no Google Colab.
   - Importação das bibliotecas utilizadas.
   - Definição dos caminhos do projeto e do dataset.

2. **Análise exploratória do dataset**
   - Verificação da estrutura das pastas.
   - Contagem de imagens por classe.
   - Análise da distribuição das classes `GOOD`, `FAIR` e `POOR`.

3. **Pré-processamento das imagens**
   - Padronização do tamanho das imagens.
   - Conversão e tratamento das imagens para uso nos modelos.
   - Demonstração visual das etapas de pré-processamento.

4. **Data augmentation**
   - Aplicação de transformações nas imagens de treinamento.
   - Geração de variações para aumentar a diversidade do conjunto de treino.
   - As transformações são aplicadas apenas ao treinamento, preservando validação e teste.

5. **Divisão do dataset**
   - Separação dos dados em treinamento, validação e teste.
   - Uso de divisão estratificada para preservar a proporção das classes.

6. **Treinamento das redes neurais convolucionais**
   - MobileNetV2
   - ResNet50
   - EfficientNetB0
   - InceptionV3
   - DenseNet121

7. **Treinamento dos modelos clássicos**
   - Extração de características com HOG.
   - Redução de dimensionalidade com PCA.
   - Treinamento dos modelos:
     - Random Forest
     - SVM
     - XGBoost

8. **Avaliação dos modelos**
   - Cálculo de acurácia, precisão, recall e F1-Score.
   - Geração de relatórios de classificação.
   - Comparação entre modelos clássicos e CNNs.

9. **Visualização dos resultados**
   - Curvas de aprendizado.
   - Gráficos comparativos.
   - Visualização de predições.

## Organização esperada do dataset

Antes de executar o notebook, o dataset deve estar organizado conforme a estrutura abaixo:

```text
data/
└── raw/
    ├── GOOD/
    ├── FAIR/
    └── POOR/
