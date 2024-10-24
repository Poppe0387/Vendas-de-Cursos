# **📊 Vendas de Cursos - Análise de Dados** 

![Badge - Python](https://img.shields.io/badge/Made%20with-Python-blue?style=for-the-badge)
![Badge - Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=for-the-badge)
![Badge - Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-yellow?style=for-the-badge)
![Badge - License](https://img.shields.io/github/license/usuario/repositorio?style=for-the-badge)

<img src="https://www.example.com/path-to-image.jpg" alt="Project Banner" width="100%"/>

---

## **📋 Descrição do Projeto**

Este projeto foi desenvolvido para realizar uma análise completa de vendas de cursos, utilizando dados de vendas, preços e quantidade de vendas para gerar insights estratégicos. As visualizações e análises foram feitas com Python e Power BI.

---

## **🚀 Tecnologias Utilizadas**

- ![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
- `pandas`, `matplotlib`, `seaborn` para análise de dados.
- **Jupyter Notebook** para execução do código.
- **Power BI** para relatórios visuais e interativos.

---

## **📂 Estrutura do Projeto**

```bash
├── data                 # Diretório com os dados brutos
├── notebooks            # Notebooks Jupyter usados no processo
├── dashboard            # Dashboard interativo no Power BI
└── README.md            # Documentação do projeto


📊 Análises Realizadas
Verificação de Valores Nulos: Nenhum valor nulo foi encontrado.
Quantidade de Vendas por Curso: Análise gráfica que identifica os cursos mais vendidos.
Relação entre Preço Unitário e Vendas: Uma correlação visual entre o preço dos cursos e o número de vendas.
Receita Total Gerada: Cálculo do faturamento total a partir da multiplicação da quantidade de vendas pelo preço unitário.
Curso Mais Vendido: Identificação do curso mais vendido com base na quantidade de vendas.
💡 Insights Obtidos
Correlação Preço x Vendas: Cursos com preços mais acessíveis tiveram maior número de vendas.
Receita Total: A receita total gerada foi de R$ {valor}.
Curso de maior destaque: O curso {curso_mais_vendido} foi o mais vendido.
📈 Visualizações no Jupyter
1. Quantidade de Vendas por Curso
python
Copiar código
plt.figure(figsize=(10,6))
sns.barplot(x='Quantidade de Vendas', y='Nome do Curso', data=vendas)
plt.title('Quantidade de Vendas por Curso')
plt.xlabel('Quantidade de Vendas')
plt.ylabel('Nome do Curso')
plt.show()
2. Relação entre Preço Unitário e Quantidade de Vendas
python
Copiar código
plt.figure(figsize=(10,6))
sns.scatterplot(x='Preço Unitário', y='Quantidade de Vendas', data=vendas)
plt.title('Relação entre Preço Unitário e Quantidade de Vendas')
plt.xlabel('Preço Unitário')
plt.ylabel('Quantidade de Vendas')
plt.show()
📊 Dashboard Interativo no Power BI
No Power BI, você pode acessar o dashboard interativo, que apresenta uma visão clara sobre as vendas, com filtros dinâmicos para regiões, tipos de cursos e períodos de tempo.

📌 Link para o Dashboard: Acessar o Dashboard Power BI

⚙️ Como Executar o Projeto
Pré-requisitos
Python 3.9+
Bibliotecas: pandas, matplotlib, seaborn
Jupyter Notebook
1. Clone o repositório
bash
Copiar código
git clone https://github.com/usuario/repositorio.git
2. Instale as dependências
bash
Copiar código
pip install -r requirements.txt
3. Execute o Jupyter Notebook
bash
Copiar código
jupyter notebook VendasCursos.ipynb
📬 Contato
Caso tenha alguma dúvida ou queira saber mais sobre o projeto:


📝 Licença
Este projeto está licenciado sob a licença MIT - consulte o arquivo LICENSE para mais detalhes.


# Análise de Vendas de Cursos

## Descrição do Projeto
Este projeto realiza uma análise detalhada dos dados de vendas de cursos oferecidos em uma plataforma online. O objetivo principal é extrair insights valiosos a partir dos dados fornecidos, utilizando bibliotecas do Python para exploração, análise estatística e visualização dos resultados.

O conjunto de dados contém informações sobre as vendas de diferentes cursos, como o número de vendas, o preço unitário de cada curso, e a data em que as vendas ocorreram. Através dessa análise, buscamos identificar padrões de vendas, receitas geradas e outras métricas relevantes.

## Estrutura dos Dados
O arquivo CSV contém as seguintes colunas:

| Colunas      | Descrição | 
| :---        |    :----:   | 
| ID      | Identificador único de cada curso vendido       | 
| Nome do Curso   | Nome do curso vendido na plataforma        | 
| Quantidade de Vendas      | Número de vendas realizadas para cada curso | 
| Preço Unitário      | Preço unitário do curso | 
| Data      | Data da venda do curso | 


## Requisitos
Para executar o projeto, você precisa dos seguintes pacotes instalados: 

```python
pip install pandas matplotlib seaborn
```

# Execução do Código
Passo 1: Carregar o Arquivo CSV
Carregue os dados do arquivo CSV e faça uma análise inicial para entender a estrutura do conjunto de dados.

```python
import pandas as pd
```

# Carregar o CSV
file_path = 'VendasDeCursos.csv'
data = pd.read_csv(file_path)
Passo 2: Exploração dos Dados
Exibir as primeiras linhas do dataset e verificar se há valores nulos ou anomalias.

python
Copiar código
# Exibir as primeiras linhas do dataset
print(data.head())

# Verificar se há valores nulos
print(data.isnull().sum())
Passo 3: Análise Descritiva
Calcular estatísticas descritivas para entender a distribuição dos dados numéricos (ex: preço e quantidade de vendas).

python
Copiar código
# Estatísticas descritivas
print(data.describe())
Passo 4: Cálculo da Receita Total
Calcular a receita total gerada pela venda dos cursos e identificar qual curso gerou a maior receita.

python
Copiar código
# Calcular a receita total
data['Receita'] = data['Quantidade de Vendas'] * data['Preço Unitário']
receita_total = data['Receita'].sum()

print(f"Receita total gerada: R$ {receita_total:.2f}")
Passo 5: Identificar o Curso com Maior Número de Vendas
Determinar qual curso teve o maior número de vendas.

python
Copiar código
# Curso com o maior número de vendas
curso_mais_vendido = data.loc[data['Quantidade de Vendas'].idxmax()]
print(f"Curso mais vendido: {curso_mais_vendido['Nome do Curso']}")
Passo 6: Análise Temporal
Converter a coluna de datas para o formato datetime e analisar a tendência das vendas ao longo do tempo.

python
Copiar código
# Converter a coluna 'Data' para datetime
data['Data'] = pd.to_datetime(data['Data'])

# Agrupar e visualizar as vendas ao longo do tempo
import matplotlib.pyplot as plt

vendas_por_dia = data.groupby('Data')['Quantidade de Vendas'].sum()
vendas_por_dia.plot(kind='line', figsize=(10,6))
plt.title('Vendas ao Longo do Tempo')
plt.xlabel('Data')
plt.ylabel('Quantidade de Vendas')
plt.grid(True)
plt.show()
Passo 7: Mês com Maior e Menor Número de Vendas
Identificar o mês com o maior e o menor número de vendas.

python
Copiar código
# Extrair o mês da coluna 'Data'
data['Mês'] = data['Data'].dt.to_period('M')

# Somar as vendas por mês
vendas_por_mes = data.groupby('Mês')['Quantidade de Vendas'].sum()

# Identificar os meses com maior e menor número de vendas
mes_mais_vendas = vendas_por_mes.idxmax()
mes_menos_vendas = vendas_por_mes.idxmin()

print(f"Mês com mais vendas: {mes_mais_vendas}")
print(f"Mês com menos vendas: {mes_menos_vendas}")
Passo 8: Visualizações Adicionais
Gráfico de barras mostrando a quantidade de vendas por curso.
Gráfico de dispersão para analisar a relação entre o preço dos cursos e o número de vendas.
python
Copiar código
import seaborn as sns

# Gráfico de barras das vendas por curso
plt.figure(figsize=(10,6))
sns.barplot(x='Quantidade de Vendas', y='Nome do Curso', data=data)
plt.title('Quantidade de Vendas por Curso')
plt.show()

# Gráfico de dispersão para a relação entre preço e quantidade de vendas
plt.figure(figsize=(10,6))
sns.scatterplot(x='Preço Unitário', y='Quantidade de Vendas', data=data)
plt.title('Relação entre Preço Unitário e Quantidade de Vendas')
plt.show()
Insights Obtidos
Receita Total: A receita total gerada por todos os cursos foi de R$ X.
Curso Mais Vendido: O curso com o maior número de vendas foi o "Curso Y", com Z vendas.
Mês Mais Vendido: O mês com o maior número de vendas foi "Mês X", enquanto "Mês Y" foi o que teve menos vendas.
Relação Preço x Vendas: Cursos com preços mais altos tendem a ter menor quantidade de vendas, enquanto cursos mais baratos vendem em maior quantidade, como esperado.
Tendência Temporal: As vendas ao longo do tempo mostraram picos em datas específicas, o que pode indicar promoções ou eventos especiais.
Conclusão
Este projeto forneceu uma análise detalhada dos dados de vendas de cursos, gerando insights valiosos sobre o desempenho dos cursos, as receitas e a dinâmica das vendas ao longo do tempo. Essas informações podem ser usadas para otimizar estratégias de marketing e ajustar preços para maximizar as vendas e o lucro da plataforma.
