# Predição de Doenças Cardíacas utilizando Machine Learning

Projeto acadêmico desenvolvido para a disciplina de Programação Avançada, implementando modelos de Machine Learning para predição de doenças cardíacas utilizando o Heart Disease Dataset.

## 📋 Sobre o Projeto

Este projeto implementa e compara três algoritmos de Machine Learning para classificação de doenças cardíacas:

- **Regressão Logística**: Modelo linear interpretável e eficiente
- **Random Forest**: Ensemble method robusto com alta capacidade preditiva
- **Support Vector Machine (SVM)**: Classificador com kernel RBF para capturar relações não lineares

O dataset utilizado contém informações clínicas e demográficas de 1025 pacientes, com 14 características relevantes para o diagnóstico cardiovascular.

## 🗂️ Estrutura do Projeto

```
pgavancada/
├── data/                          # Diretório para datasets
│   └── heart.csv                  # Heart Disease Dataset
├── notebooks/                     # Notebooks Jupyter
│   ├── 01_exploratory_analysis.ipynb
│   └── 02_model_training.ipynb
├── paper/                         # Artigo científico IEEE
│   └── main.tex                   # Template LaTeX do artigo
├── src/                           # Código fonte Python
│   └── main.py                    # Implementação principal
├── requirements.txt               # Dependências do projeto
└── README.md                      # Este arquivo
```

## 🚀 Instalação e Configuração

### Pré-requisitos

- Python 3.8 ou superior
- pip (gerenciador de pacotes Python)
- Git (para clonar o repositório)

### Passos para Instalação

1. **Clone o repositório:**
```bash
git clone https://github.com/seu-usuario/pgavancada.git
cd pgavancada
```

2. **Crie um ambiente virtual (recomendado):**
```bash
python -m venv venv

# No Linux/Mac:
source venv/bin/activate

# No Windows:
venv\Scripts\activate
```

3. **Instale as dependências:**
```bash
pip install -r requirements.txt
```

## 📊 Dataset

O **Heart Disease Dataset** utilizado neste projeto está disponível no [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/heart+disease).

### Download do Dataset

1. Acesse o link: https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction
2. Baixe o arquivo `heart.csv`
3. Coloque o arquivo na pasta `data/` do projeto

**Nota:** Se o dataset não estiver disponível no link acima, você pode usar uma versão alternativa disponível em:
- UCI Repository: https://archive.ics.uci.edu/ml/datasets/heart+disease
- Kaggle: https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset

### Características do Dataset

- **Número de instâncias:** 1025
- **Número de características:** 14
- **Tipo de problema:** Classificação binária
- **Variável alvo:** HeartDisease (0 = ausente, 1 = presente)

## 💻 Como Executar

### Opção 1: Executar o script principal

```bash
cd src
python main.py
```

O script realizará todas as etapas:
- Carregamento e análise exploratória
- Pré-processamento dos dados
- Treinamento dos três modelos
- Avaliação e comparação
- Geração de visualizações

### Opção 2: Executar notebooks Jupyter

1. **Inicie o Jupyter Notebook:**
```bash
jupyter notebook
```

2. **Abra e execute os notebooks na ordem:**
   - `notebooks/01_exploratory_analysis.ipynb` - Análise exploratória
   - `notebooks/02_model_training.ipynb` - Treinamento e avaliação

### Opção 3: Usar em ambiente interativo Python

```python
from src.main import HeartDiseasePredictor

# Inicializar predictor
predictor = HeartDiseasePredictor('data/heart.csv')

# Carregar dados
predictor.load_data()

# Pré-processar
predictor.preprocess_data()

# Treinar modelos
predictor.train_models()

# Avaliar
predictor.evaluate_models()

# Visualizações
predictor.plot_confusion_matrices()
predictor.plot_roc_curves()
predictor.plot_feature_importance()
```

## 📈 Resultados Esperados

O código gera os seguintes arquivos de saída:

- `confusion_matrices.png` - Matrizes de confusão dos três modelos
- `roc_curves.png` - Curvas ROC comparativas
- `feature_importance.png` - Importância das características (Random Forest)
- `results_comparison.csv` - Tabela comparativa de métricas

### Métricas de Desempenho

Os modelos são avaliados utilizando as seguintes métricas:

- **Accuracy** (Acurácia)
- **Precision** (Precisão)
- **Recall** (Revocação)
- **F1-Score**
- **AUC-ROC** (Área sob a curva ROC)

### Resultados Típicos

- **Regressão Logística:** ~85% de acurácia
- **Random Forest:** ~88% de acurácia
- **SVM (RBF):** ~87% de acurácia

*Nota: Os resultados podem variar ligeiramente dependendo da divisão treino/teste.*

## 📄 Artigo Científico

O artigo científico completo seguindo o template IEEE está disponível em `paper/main.tex`.

### Compilação do Artigo LaTeX

Para gerar o PDF do artigo:

```bash
cd paper
pdflatex main.tex
bibtex main  # Se houver referências
pdflatex main.tex
pdflatex main.tex
```

**Requisitos para compilação:**
- LaTeX distribution (TeX Live, MiKTeX, etc.)
- Pacotes IEEEtran

### Estrutura do Artigo

1. Abstract e Keywords
2. Introdução
3. Fundamentação Teórica
4. Metodologia
5. Proposta e Implementação
6. Resultados
7. Discussão
8. Conclusão
9. Referências

## 🛠️ Tecnologias Utilizadas

- **Python 3.9+**
- **scikit-learn 1.0+** - Machine Learning
- **pandas** - Manipulação de dados
- **numpy** - Operações numéricas
- **matplotlib** - Visualizações básicas
- **seaborn** - Visualizações estatísticas
- **Jupyter Notebook** - Ambiente interativo
- **LaTeX** - Formatação do artigo

## 👥 Autores

- Guilherme Romualdo
- Maria Fernanda Jatobá

## 📚 Referências

- UCI Machine Learning Repository - Heart Disease Dataset
- Scikit-learn Documentation
- IEEE Template para artigos científicos

## 📝 Licença

Este projeto foi desenvolvido para fins acadêmicos. O código está disponível para uso educacional.

## 🤝 Contribuições

Este é um projeto acadêmico desenvolvido como trabalho de conclusão de disciplina. Contribuições externas não são esperadas, mas sugestões são bem-vindas.

## ⚠️ Avisos Importantes

1. **Uso Educacional:** Este projeto foi desenvolvido exclusivamente para fins educacionais e acadêmicos.

2. **Não substitui diagnóstico médico:** Os modelos desenvolvidos são para fins de pesquisa e não devem ser utilizados para diagnóstico médico real sem validação clínica adequada.

3. **Dataset:** Certifique-se de usar o dataset correto e verificar sua licença de uso.

## 📧 Contato

Para dúvidas ou questões sobre o projeto, entre em contato através dos e-mails dos autores listados acima.

---

**Desenvolvido como projeto acadêmico para a disciplina de Programação Avançada**

