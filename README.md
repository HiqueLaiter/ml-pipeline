# Action da Pipeline de Machine Learning

Este repositório contém um pipeline automatizado de Machine Learning que, a cada push, executa o treinamento de um modelo de classificação e gera um relatório de desempenho.

## Estrutura do Projeto

- `data/sample.csv`: Dataset de exemplo utilizado para treinamento e avaliação.
- `train.py`: Script Python que realiza a leitura dos dados, treino do modelo, avaliação e geração do relatório.
- `requirements.txt`: Dependências necessárias para rodar o script.
- `.github/workflows/ml.yml`: Workflow do GitHub Actions que automatiza o processo de treinamento e geração do relatório.

## GitHub Actions

Foi configurado um workflow que dispara em cada push no repositório. As etapas são:

1. Checkout do código.
2. Configuração do ambiente Python (versão 3.11).
3. Instalação das dependências listadas no `requirements.txt`.
4. Execução do script `train.py` para treinar o modelo e gerar o relatório.
5. Upload do arquivo `report.txt` como artefato da execução, contendo métricas de avaliação (acurácia, precisão, recall e F1-score).

### Visualização da execução

Acesse a aba **Actions** do repositório para acompanhar a execução do workflow. Você pode verificar o status, logs detalhados e baixar o relatório gerado.

## Como usar localmente

1. Clone o repositório:

   ```bash
   git clone <URL-do-repositório>
   cd ml-pipeline
