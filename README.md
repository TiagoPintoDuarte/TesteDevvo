# Teste DEVVO 🚀

## Visão Geral 📋

Este repositório contém um conjunto de testes de API utilizando Newman, Postman e Integração com Slack


## Requisitos ✅


- **Node.js** (versão 12 ou superior) instalado para executar o Newman.
- **Postman** para criar e exportar a coleção de testes.
- **Newman** instalado globalmente via npm para a execução dos testes via linha de comando.
- **Conta no Slack** e um webhook configurado para receber as notificações dos testes.

## Configuração ⚙️


### 1. Instalação do Newman 🛠️

- Instale o Newman globalmente em seu ambiente com o seguinte comando:
  ```bash
  npm install -g newman
  ```
- Instale o reporter

  ```bash
  npm install -g newman-reporter-htmlextra
  ```

### 2. Execução dos Testes com Newman 🏃‍♂️

- Para executar sua coleção de testes exportada do Postman, use o comando abaixo:
  ```bash
  newman run <nome_da_colecao>.json
  ```
- Caso queira gerar relatórios mais detalhados, você pode usar opções como:
  ```bash
  newman run <nome_da_colecao>.json -r htmlextra
  ```

### 3. Integração CI ⚙️

- Integrei o processo de execução dos testes com um pipeline de CI para automatizar a execução dos testes a cada nova mudança no código.

  - **Execução Automatizada**: Os testes são executados automaticamente em cada `push` para a branch `master` e em pull requests.
  - **Notificação no Slack**: Caso os testes falhem, uma notificação é enviada ao Slack para garantir que a equipe esteja ciente dos problemas.

## Referências 📚

- [Documentação Postman](https://learning.postman.com/docs/getting-started/introduction/)
- [Documentação Newman](https://www.npmjs.com/package/newman)
- [Integração de Webhooks no Slack](https://api.slack.com/messaging/webhooks).

