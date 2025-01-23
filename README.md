# curso-mlflow
O uso dessa ferramenta viabilisará a produção e gestão de diferentes modelos treinados. Bem como auxiliará na maneira como os modelos são selecionados para produção.

Todo material está no YouTube no Canal [@teomewhy](https://www.youtube.com/@teomewhy)

Repositorio base: [TeoMeWhy](https://github.com/TeoMeWhy/curso-mflow)


# Estrutura do Projeto
```
.
├── mlflow-server
│   ├── mlartifacts
│   ├── mlruns
│   └── requirements.txt
├── model_churn
│   ├── data
│   ├── requirements.txt
│   └── train.py
└── README.md
```

# mlflow-server

É aqui que os artefatos serão gerados a partir do MLFlow. É o lugar onde você deve executar os comandos:
```
cd mlflow-server
conda create --name mlflow-server python=3.12
conda activate mlflow-server
pip install mlflow
mlflow server
```
Após executar mlflow server, ir até o endereço criado, no caso http://127.0.0.1:5000, mas o ideal é que fique na cloud.

# Sempre que precisar subir o servidor do MLFlow, pode executar: ml-churn
```
cd mlflow-server
conda activate mlflow-server
mlflow server
```

Assim que você criar os primeiros modelos e exeprimentos, as demais pastas serão criadas.

# model_churn

Por melhores práticas, o ambiente de Machine Learning é separado do ambiente do MLFlow

Esse é o diretório do nosso projeto de Machine Learning. É onde contruímos o nosso modelo, armazenamos os dados, e todo código necessário para o modelo ser treinado e executado.

Para construir o ambiente necessário, execute os comandos:
```
cd model_churn
conda create --name ml-churn python=3.12
conda activate ml-churn
pip install -r requirements.txt
```
