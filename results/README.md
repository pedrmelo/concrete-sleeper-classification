# 📊 Resultados

Esta pasta reúne os resultados obtidos durante os experimentos de classificação da qualidade de dormentes de concreto nas classes **GOOD** e **POOR**.

Os resultados incluem métricas dos modelos clássicos de Machine Learning e das arquiteturas de Redes Neurais Convolucionais avaliadas no projeto.

## 🤖 Modelos avaliados

### Machine Learning clássico

- Random Forest
- Support Vector Machine (SVM)
- XGBoost

Os modelos clássicos utilizam características extraídas das imagens por meio de **HOG**, seguidas de redução de dimensionalidade com **PCA**.

### Redes Neurais Convolucionais

Foram avaliadas as seguintes arquiteturas:

- MobileNetV2
- ResNet50
- InceptionV3
- DenseNet121
- EfficientNetB0

## 📈 Principais resultados

### Modelos Clássicos

| Modelo | Acurácia | Precisão | Recall | F1-score |
| :--- | :---: | :---: | :---: | :---: |
| **Random Forest** | 96,67% | 96,69% | 96,67% | 96,67% |
| **SVM** | 97,78% | 97,78% | 97,78% | 97,78% |
| **XGBoost** | 96,67% | 96,69% | 96,67% | 96,67% |

### Modelos de Deep Learning

| Modelo | Acurácia | Precisão | Recall | F1-score |
| :--- | :---: | :---: | :---: | :---: |
| **InceptionV3** | 95,56% | 95,56% | 95,56% | 95,56% |
| **DenseNet121** | 96,67% | 96,69% | 96,67% | 96,67% |
| **MobileNetV2** | 98,89% | 98,91% | 98,89% | 98,89% |
| **ResNet50** | 96,67% | 96,69% | 96,67% | 96,67% |
| **EfficientNetB0** | 95,56% | 95,56% | 95,56% | 95,56% |


## 📌 Observação

As métricas apresentadas nos arquivos correspondem aos experimentos realizados no notebook principal do projeto.

Para reprodução completa dos resultados, consulte o notebook:

`notebooks/01_pipeline_classificacao_dormentes.ipynb`
