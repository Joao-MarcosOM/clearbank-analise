# clearbank-analise

Projeto desenvolvido como desafio prático do módulo **Análise de Dados e Inteligência de Negócios com IA** (Rocketseat).

## Sobre o projeto

A ClearBank é uma fintech fictícia cuja equipe de operações exporta mensalmente o histórico de transações dos clientes em CSV, mas o arquivo costuma chegar com problemas: campos vazios, valores inválidos, datas mal formatadas etc.

Este notebook lê, valida e limpa esses dados usando apenas o módulo `csv` nativo do Python (sem pandas), calcula métricas financeiras mensais, sinaliza transações potencialmente suspeitas, exibe um relatório formatado no terminal e exporta o resultado em JSON.

## Como executar

1. Abra o arquivo `desafio-final.ipynb` no [Google Colab](https://colab.research.google.com/) ou em um Jupyter Notebook local (Python 3.10+).
2. Execute todas as células em ordem, de cima para baixo.
   - A primeira célula de código gera o arquivo `transacoes.csv` de teste automaticamente — não é necessário enviar nenhum arquivo externo.
   - As demais células definem as funções de leitura, validação, geração de métricas e exportação.
   - A **Célula de Execução Principal** (última célula) roda todo o fluxo e imprime o relatório final.

## O que o notebook gera

- **`transacoes.csv`** — base de teste com 15 registros válidos (distribuídos em 3 meses) e 5 registros inválidos, criada pelo próprio notebook.
- **Relatório no terminal**, com:
  - Resumo da limpeza (total de linhas lidas, válidas e inválidas)
  - Período analisado (data mais antiga → mais recente, em dias)
  - Métricas mensais: quantidade de transações, total de crédito, total de débito, saldo, média, maior e menor valor
  - Lista de transações suspeitas (valor acima de R$ 10.000,00)
- **`relatorio.json`** — arquivo com o resultado completo da análise (resumo mensal e transações suspeitas), gerado automaticamente ao final da execução.

## Estrutura do repositório

```
clearbank-analise/
├── desafio-final.ipynb   # notebook com o código e as saídas salvas
└── README.md             # este arquivo
```

## Tecnologias utilizadas

- Python 3
- Módulos nativos: `csv`, `json`, `datetime`
