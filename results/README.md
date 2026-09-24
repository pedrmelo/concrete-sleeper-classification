# 📊 Resultados

Esta pasta reúne os resultados obtidos durante os experimentos de classificação da qualidade de dormentes de concreto nas classes **GOOD**, **FAIR** e **POOR**.

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

Entre os modelos clássicos, os resultados foram:

Modelo | Acuracia | Precisão | Recall | F1-score |
Random Forest | 89,90% | 89,88% | 89,90% | 89,88% |
SVM | 95,12% | 95,30% | 95,12% | 95,11% |
XGBoost | 90,24% | 90,99% | 90,24% | 90,07% |

Entre os modelos deep learning, os resultados foram:

Modelo | Acuracia | Precisão | Recall | F1-score |
InceptionV3 | 97,56% | 97,58% | 97,56% | 97,57% |
DenseNet121 | 94,08% | 94,58% | 94,08% | 94,04% |
MobileNetV2 | 97,21% | 97,27% | 97,21% | 97,21% |
ResNet50 | 96,86% | 96,88% | 96,86% | 96,87% |
MobileNetV2 | 74,22% | 76,76% | 74,22% | 74,78% |


## 📌 Observação

As métricas apresentadas nos arquivos correspondem aos experimentos realizados no notebook principal do projeto.

Para reprodução completa dos resultados, consulte o notebook:

`notebooks/01_pipeline_classificacao_dormentes.ipynb`
