# Projeto: Inteligência Artificial e Previsões - Score de Crédito

Resumo
-------
Este repositório contém um projeto didático para criar um modelo de machine learning que prevê o score de crédito de clientes (Poor / Standard / Good). O notebook principal realiza carregamento e pré-processamento de dados, treinamento de modelos (Random Forest e KNN), avaliação e previsão para novos clientes.

Conteúdo do repositório
-----------------------
- `iaprevisoes.ipynb` - Notebook principal com código para preparação dos dados, treinamento dos modelos, avaliação e predição em novos clientes.
- `clientes.csv` - Base de dados usada para treinar e avaliar os modelos.
- `novos_clientes.csv` - Base de dados com novos clientes para realizar previsões.

Objetivo
--------
Criar um pipeline simples de machine learning que:
1. Lê e inspeciona os dados dos clientes;
2. Converte variáveis categóricas em representações numéricas;
3. Separa dados em treino e teste;
4. Treina e compara modelos (Random Forest e KNN);
5. Gera previsões para novos clientes.

Requisitos
----------
- Python 3.8+ (recomendado)
- pacotes Python:
  - pandas
  - scikit-learn

Instalação rápida
-----------------
Crie um ambiente virtual e instale as dependências:

```powershell
python -m venv .venv; .\.venv\Scripts\Activate.ps1; pip install -U pip; pip install pandas scikit-learn
```

Como usar
---------
1. Abra o notebook `iaprevisoes.ipynb` em Jupyter Notebook / JupyterLab / VS Code (editor de notebooks).
2. Execute as células uma a uma na ordem apresentada.

Pontos importantes ao executar
------------------------------
- As colunas categóricas são codificadas com `LabelEncoder` e os objetos `codificador1`, `codificador2`, `codificador3` são utilizados para transformar os dados novos. Por isso é importante não re-ajustar (`fit`) esses codificadores nos dados novos — o notebook já foi ajustado para usar `transform()` ao processar `novos_clientes.csv`.
- Se houver categorias nos dados novos que não existiam no conjunto de treino, `LabelEncoder.transform()` pode falhar. Nesses casos, é necessário tratar ou mapear as novas categorias antes de transformar (ex.: mapear para um valor especial ou re-treinar os codificadores com cuidado).

Licença
-------
Este é um projeto educacional. Adapte e reutilize conforme necessário.