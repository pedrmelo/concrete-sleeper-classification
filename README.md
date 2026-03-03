# Classificação Automatizada de Dormentes de Concreto

## 📋 Sobre

Sistema de classificação de qualidade de dormentes ferroviários de concreto 
usando Redes Neurais Convolucionais (CNNs) com transfer learning.

## 🎯 Objetivos

- Comparar 5 arquiteturas de CNNs (MobileNetV2, ResNet50, InceptionV3, 
  DenseNet121, EfficientNetB0)
- Classificar dormentes em 3 classes: GOOD, FAIR, POOR
- Analisar viabilidade para sistemas embarcados
- Interpretabilidade via Grad-CAM

## 🏗️ Arquiteturas Avaliadas

| Arquitetura     | Parâmetros | Paradigma                        |
|-----------------|------------|----------------------------------|
| MobileNetV2     | 3.4M       | Depthwise separable convolutions |
| ResNet50        | 25.6M      | Skip connections                 |
| InceptionV3     | 23.8M      | Multi-scale convolutions         |
| DenseNet121     | 8.0M       | Dense connections                |
| EfficientNetB0  | 5.3M       | Neural Architecture Search       |

## 🛠️ Tecnologias

- Python 3.10
- TensorFlow 2.15.0
- OpenCV 4.8.0

## 📁 Estrutura do Projeto

```
concrete-sleeper-classification/
├── data/               # Dataset
├── notebooks/          # Jupyter Notebooks
├── src/                # Código-fonte
├── scripts/            # Scripts executáveis
├── models/             # Modelos treinados
├── results/            # Resultados e visualizações
└── docs/               # Documentação
```

## 🚀 Como Usar

Em desenvolvimento...

## 📧 Contato

[Seu email]

## 📝 Licença

MIT License


📄 LICENSE (opcional mas recomendado)
────────────────────────────────────────────────────────────────────────────
Nome do arquivo: LICENSE
Conteúdo:

MIT License

Copyright (c) 2026 [Seu Nome Completo]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
