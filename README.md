# Explorando a Tabela FIPE com Pandas

Notebook desenvolvido para praticar **análise e manipulação de dados com Python e Pandas**, utilizando um conjunto de dados baseado no histórico de preços de veículos da Tabela FIPE.

O projeto explora informações sobre veículos, preços e anos de modelo por meio de consultas, filtros, ordenação, estatísticas e visualizações gráficas.

## Sobre o projeto

O objetivo deste notebook é aplicar conceitos fundamentais de **Data Science e análise de dados** em um conjunto de dados do setor automotivo.

Durante os exercícios, são utilizadas operações do Pandas para:

* Inspecionar e compreender um DataFrame;
* Filtrar registros de acordo com determinados critérios;
* Ordenar dados;
* Calcular estatísticas básicas;
* Identificar os veículos de maior valor;
* Criar visualizações com Matplotlib;
* Interpretar a distribuição dos preços dos veículos.

## Tecnologias utilizadas

* **Python**
* **Jupyter Notebook**
* **Pandas**
* **Matplotlib**

## Estrutura dos dados

O notebook utiliza o arquivo:

```text
tabelafipe.csv
```

O arquivo CSV deve estar no mesmo diretório do notebook para que os dados sejam carregados corretamente.

Exemplo de carregamento:

```python
import pandas as pd
import matplotlib.pyplot as plt

dados = pd.read_csv("tabelafipe.csv")
df = pd.DataFrame(dados)
```

Entre as informações utilizadas no projeto estão:

| Coluna      | Descrição         |
| ----------- | ----------------- |
| `valor`     | Valor do veículo  |
| `anoModelo` | Ano do modelo     |
| `modelo`    | Modelo do veículo |

## Conteúdos praticados

O notebook é dividido em quatro níveis de dificuldade.

### Nível 1 — Conhecendo a tabela

Operações básicas para compreender a estrutura do DataFrame:

* `head()`
* `tail()`
* `shape`

### Nível 2 — Filtrando e ordenando

Manipulação dos dados para encontrar informações específicas:

* Filtros condicionais;
* Contagem de registros;
* `sort_values()`;
* Ordenação crescente e decrescente.

Exemplo:

```python
df[df["valor"] > 100000]
```

### Nível 3 — Curiosidades e estatísticas

Aplicação de operações estatísticas simples:

* Média dos preços;
* Média dos anos de modelo;
* Identificação do veículo de maior valor;
* `mean()`;
* Ordenação para encontrar valores extremos.

Exemplo:

```python
media_valor = df["valor"].mean()
```

### Nível 4 — Visualização

Criação de gráficos para facilitar a interpretação dos dados:

* Gráfico de barras;
* Histograma;
* Distribuição dos preços;
* Comparação entre os veículos de maior valor.

Exemplo:

```python
df["valor"].plot(kind="hist", bins=20)
```

## Exercícios

O notebook contém **10 exercícios práticos**, começando por operações básicas e avançando gradualmente para análise estatística e visualização.

| Exercício | Conteúdo                  |
| --------- | ------------------------- |
| 01        | Primeiras 10 linhas       |
| 02        | Últimas 5 linhas          |
| 03        | Dimensões do DataFrame    |
| 04        | Filtro por preço          |
| 05        | Veículos mais antigos     |
| 06        | Veículos mais recentes    |
| 07        | Média de preços e anos    |
| 08        | Veículo de maior valor    |
| 09        | Top 10 veículos por preço |
| 10        | Distribuição dos preços   |

## Objetivos de aprendizagem

Ao finalizar o notebook, espera-se que o estudante consiga:

* Carregar arquivos CSV utilizando Pandas;
* Trabalhar com DataFrames;
* Selecionar e filtrar dados;
* Ordenar registros;
* Realizar cálculos estatísticos básicos;
* Identificar informações relevantes em grandes conjuntos de dados;
* Criar gráficos simples;
* Interpretar resultados obtidos por meio da análise de dados.

## Como executar

1. Instale o Python.
2. Instale as bibliotecas necessárias:

```bash
pip install pandas matplotlib jupyter
```

3. Coloque os arquivos na mesma pasta:

```text
├── explorando-tabela-fipe.ipynb
└── tabelafipe.csv
```

4. Inicie o Jupyter Notebook:

```bash
jupyter notebook
```

5. Abra o arquivo `.ipynb` e execute as células na ordem.

## Observação

Os resultados apresentados pelo notebook dependem dos dados presentes no arquivo `tabelafipe.csv`. Alterações ou atualizações no conjunto de dados podem modificar os valores obtidos nos exercícios.

## Licença

Este projeto está disponível para fins educacionais e de estudo.

---

Desenvolvido como prática de **Python, Pandas e análise de dados**.
