# Consumo e Tratamento de Dados de Carrinho em Loja Fake

## Descrição
Este projeto tem como objetivo consumir dados da [Fake Store API](https://fakestoreapi.com/docs), realizar o tratamento desses dados e persistir as informações em uma tabela do Big Query. A análise foca em identificar o identificador de usuário, a data mais recente em que o usuário adicionou produtos ao carrinho e a categoria com mais produtos adicionados ao carrinho.

## Status do projeto
Versão 1.0

## Tecnologias utilizadas
Python 3.9.13 | Bibliotecas: pandas, requests, pandas_gbq, google.oauth2

## Sobre os Arquivos
- `data/arquivo_tratado.csv`: Arquivo CSV resultante da transformação dos dados, contendo informações sobre usuários, datas de adição ao carrinho e categorias mais adicionadas.
- `scripts/notebook.ipynb`: Jupyter Notebook contendo o código-fonte utilizado para realizar o consumo, tratamento dos dados e carregamento dos resultados.
- `scripts/GBQ.json`: Arquivo de credenciais para autenticação ao Google BigQuery, utilizado para carregar os dados no BigQuery.

## Como usar

1. Clone o repositório em sua máquina local.
2. Certifique-se de ter as dependências instaladas. Caso não tenha, instale-as utilizando o gerenciador de pacotes pip.
3. Configure suas credenciais do Google Cloud. Para isso, siga os passos abaixo:
  - Acesse o menu de navegação do Google Cloud: Menu de navegação > IAM e administrador > Contas de serviço.
  - Escolha a conta de serviço desejada.
  - Vá para a seção "Chaves" e clique em "Adicionar chave".
  - Selecione o formato JSON e clique em "Baixar".
  - Renomeie o arquivo para GBQ.json
4. Execute o arquivo `notebook.ipynb` para consumir os dados da API, processá-los, armazená-los no BigQuery e gerar o arquivo `arquivo_tratado.csv`

## Resultado final
A tabela final será salva em uma tabela no Big Query:

<img src="https://drive.google.com/uc?id=1_ljLM9CEPSLg-tu7AuxQo-dJRWWO6PdP">

E poderá ser observada também no `data/arquivo_tratado.csv`.

## Indicações de melhorias futuras
- *Persistência em Camadas*: Considerar uma estratégia de armazenamento em camadas, como os modelos de dados Gold, Silver e Bronze, para que os dados brutos não se percam. Embora não tenha sido necessário nesta análise pontual, essa abordagem permitirá maior organização e reutilização dos dados em análises futuras, especialmente à medida que o projeto evolui.
- *Implementação de Pipeline*: Considerar a utilização de ferramentas de orquestração como o Airflow para automatizar o fluxo de trabalho, facilitando a execução programada e a manutenção dos processos de ETL.
- *Escalabilidade com Spark*: À medida que o volume de dados aumenta, utilizar o Apache Spark para processamento em larga escala se tornará essencial. Isso garantirá eficiência e agilidade na manipulação de grandes volumes de dados.
- *Monitoramento*: Avaliar a inclusão de monitoramento e logging nas etapas do processo para facilitar a identificação de erros e a otimização do desempenho, melhorando a confiabilidade e a manutenção do sistema.

## Contato

Desenvolvedora do Projeto: Isabela Vitoriano

• Linkedin: [https://www.linkedin.com/in/isabela-vitoriano/](https://www.linkedin.com/in/isabela-vitoriano/)

• E-mail: [isabelavitoriano.ss@gmail.com](isabelavitoriano.ss@gmail.com)
  
