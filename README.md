# Avaliação da qualidade de dormentes de concreto baseado em visão computacional.

## 🎯 Objetivos

O trabalho tem como objetivo investigar e responder 3 principais questões:

1) Modelos de aprendizado profundo baseados em redes neurais convolucionais são capazes de classificar automaticamente a qualidade de dormentes de concreto a partir de imagens?
(2) Como o desempenho das arquiteturas convolucionais se compara ao de modelos clássicos de aprendizado de máquina baseados em descritores manuais?
(3)  Quais modelos apresentam melhor equilíbrio entre desempenho preditivo e viabilidade computacional para uma possível aplicação embarcada?

## 🏗️ Arquiteturas Avaliadas

| Arquitetura     | 
|-----------------|
| Random Forest   |
| SVM             |
| XGBoost         |
| MobileNetV2     | 
| ResNet50        |
| InceptionV3     |
| DenseNet121     | 
| EfficientNetB0  |

## 📁 Estrutura do Projeto

```
concrete-sleeper-classification/
├── data/               # Dataset
├── notebooks/          # Notebooks do projeto
├── results/            # Resultados e visualizações
└── docs/               # Documentação
```

## 🚀 Como Usar
### ⭐ Recomendação: Google Colab (Mais Fácil)

A forma **mais simples e rápida** de executar este projeto é usando **Google Colab**, que oferece:
- ✅ GPU NVIDIA gratuita (K80 ou T4)
- ✅ Nenhuma instalação necessária
- ✅ Ambiente pré-configurado com TensorFlow, PyTorch, etc.
- ✅ Execução mais rápida que CPU local
- ✅ Salva resultados automaticamente no Google Drive

#### **1. Executar no Google Colab (Recomendado)**

**Opção A: Abrir Notebook Direto do Repositório**

1. Acesse o notebook no GitHub
2. Clique no badge abaixo para abrir no Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/pedrmelo/concrete-sleeper-classification/blob/main/notebooks/01_pipeline_classificacao_dormentes.ipynb)

**Opção B: Abrir Manualmente**

1. Acesse [Google Colab](https://colab.research.google.com/)
2. Vá em **Arquivo → Abrir notebook**
3. Clique em **GitHub**
4. Cole: `github.com/seu_usuario/concrete-sleeper-classification`
5. Selecione `notebooks/01_pipeline_classificacao_dormentes.ipynb`

#### **2. Configurar GPU no Colab**

Na primeira célula do notebook ou em **Runtime → Change runtime type**:

```python
# Verificar se GPU está disponível
import tensorflow as tf
print(tf.config.list_physical_devices('GPU'))
```

Se não aparecer GPU, abra **Runtime → Change runtime type** e selecione **GPU** como acelerador.

#### **3. Montar Google Drive**

Execute esta célula no início do notebook:

```python
from google.colab import drive
drive.mount('/content/drive')
```

Autorize o acesso ao seu Google Drive.

#### **4. Baixar Dataset**

O dataset está disponível na seção **Releases** deste repositório no GitHub.

Faça o download do arquivo `.zip` da versão desejada e, no Google Colab, execute:

```python
# Fazer upload do arquivo .zip do dataset
from google.colab import files

uploaded = files.upload()
```

#### **5. Executar o Notebook**

- Clique em **Runtime → Run all** ou execute célula por célula
- O Colab salvará progresso automaticamente
- Resultados serão salvos em `drive/MyDrive/concrete-sleeper-classification/results/`

---

### 💻 Alternativa: Executar Localmente

Se preferir rodar na sua máquina:

#### **Pré-requisitos**

- Python 3.8 ou superior
- pip (gerenciador de pacotes Python)

#### **1. Clonar o Repositório**

```bash
git clone https://github.com/seu_usuario/concrete-sleeper-classification.git
cd concrete-sleeper-classification
```

#### **2. Criar Ambiente Virtual**

**No Windows:**
```bash
python -m venv venv
venv\Scripts\activate
```

**No Linux/macOS:**
```bash
python3 -m venv venv
source venv/bin/activate
```

#### **3. Instalar Dependências**

```bash
pip install -r requirements.txt
```

#### **4. Baixar Dataset**

**Dataset na seção Releases**
- Acesse Releases nesse projeto
- Baixe o ZIP
- Extraia para `data/`

#### **5. Verificar Estrutura de Diretórios**

```
concrete-sleeper-classification/
├── data/
│   ├── FAIR/
│   ├── GOOD/
│   └── POOR/
├── notebooks/
│   └── 01_pipeline_classificacao_dormentes
├── results/
├── requirements.txt
└── README.md
```

#### **6. Executar o Notebook Localmente**

---

### 🔧 Estrutura do Notebook

O notebook está dividido em 7 seções principais:

| Seção | Descrição |
|-------|-----------|
| 1 | Importação e Configuração
| 2 | Carregamento do Dataset
| 3 | Pré-processamento
| 4 | Deep Learning (MobileNetV2, ResNet, Inception)
| 5 | Extração de Features (HOG)
| 6 | Modelos Clássicos (RF, SVM, XGB)
| 7 | Comparação Final

---

### 🎯 Variáveis Principais

Modifique no início do notebook conforme necessário:

```python
# Caminhos
DATA_PATH = "./data/"
RESULTS_PATH = "./results/"

# Configurações de Imagem
IMAGE_SIZE = 224  # pixels
RANDOM_STATE = 42

# Deep Learning
EPOCHS = 50
BATCH_SIZE = 32
LEARNING_RATE = 0.001

```

### 📊 Outputs Esperados

Após execução, você terá em `results/`:

**Métricas (CSV):**
- `classical_models_metrics.csv`
- `cnn_models_metrics.csv`
- `all_models_comparison.csv`

**Gráficos (PNG):**
- Acurácia por modelo
- Curvas de treinamento
- Matrizes de confusão
- Comparações visuais

**Modelos Salvos:**
- `.h5` (Keras/TensorFlow)
- `.joblib` (sklearn)

---

## 📧 Contato

pedrommelo01@gmail.com
