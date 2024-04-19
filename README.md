# Projeto-Venda-de-carros
É uma concessionária de carros que vende diversos modelos de automóveis. 
O objetivo deste projeto é projetar e desenvolver um Dashboard de Vendas de Carros dinâmico e interativo usando o Power BI. Com o Dashboard conseguimos visualizar KPIs críticos relacionados as vendas de carros, ajudando a entender o desempenho das vendas ao longo do tempo e a tomar decisões orientadas por dados.
O Dashboad deve fornecer insights em tempo real sobre os principais indicadores de desempenho (KPIs) relacionados aos nossos dados de vendas. Isso nos permitirá tomar decisões informadas, monitorar o progresso e identificar tendências e oportunidades de crescimento.
## Explicação das funções:
### 1: YTD (Year-to-Date) 
A função YTD em DAX é frequentemente usada para calcular medidas acumuladas ao longo do ano até a data atual.
Em outras palavras, é o total acumulado do ano até ao momento.
**Função:TOTALYTD**


#### 2: MTD (Month-to-Date
Assim como o YTD a função MTD é usada para calcular medidas acumuladas, mas especificamente para o período atual do mês.
Refere-se aos valores acumulados desde o início do mês até a data atual.
**Função:TOTALMTD**


#### 3: YOY (Year-over-Year)
A função YOY em DAX é uma medida que pode ser usada para calcular a variação percentual ou absoluta entre os valores de um determinado período e os valores correspondentes do ano anterior. Por exemplo, se  tivermos dados de vendas mensais, pode usar a função YOY para calcular quanto as vendas deste mês diferem das vendas do mesmo mês no ano passado.
Depois de se ter a métrica do ano atual e anterior,é necessário fazer uma <b>divisão</b> no Power bi.
Como estamos a analisar uma variação entre períodos, o resultado é um percentual %.


#### 4: LY (Last Year)
LY em DAX geralmente se refere a "Last Year" (Ano Passado), e é usada para calcular medidas ou valores correspondentes ao mesmo período do ano anterior.
**Função:SAMEPERIODLASTYEAR**

### Parte 1: Requisitos das Vendas (Medidas)
#### Vendas Totais do Ano até a Data (YTD) 
![image](https://github.com/lagmagalhaes/Projeto-Venda-de-carros-PBI/assets/166879716/6e93617b-0a9b-4319-b2d8-e8404c3f4f2d)


#### Vendas Totais do Mês até a Data (MTD)
![image](https://github.com/lagmagalhaes/Projeto-Venda-de-carros-PBI/assets/166879716/8d8e9fb8-b2a6-4ae0-95d9-73ddc4dc44f4)


#### Crescimento Ano a Ano (YOY) nas Vendas Totais
![image](https://github.com/lagmagalhaes/Projeto-Venda-de-carros-PBI/assets/166879716/701365c3-4aae-403a-88d0-c9a62a4a45ae)


#### Diferença entre as Vendas YTD e as Vendas do Ano Anterior até a Data (PTYD)
**Primeiro:**
![image](https://github.com/lagmagalhaes/Projeto-Venda-de-carros-PBI/assets/166879716/c179bb45-0daf-403a-9c99-4fc14b8ff336)

**Segundo:**

![image](https://github.com/lagmagalhaes/Projeto-Venda-de-carros-PBI/assets/166879716/a3d8dd40-79fe-4a83-b43b-e2698bad39c1)


#### Análise do Preço Médio:
##### Médio YTD
YTD Cars Sold = TOTALYTD(count(car_data[Car_id]), 'Date'[Date])

##### Preço Médio MTD
MTD Total Sales = TOTALMTD(sum(car_data[Price ($)]),'Date'[Date])

##### Crescimento Ano a Ano no Preço Médio
<p>Diferença entre o Preço Médio YTD e o Preço Médio PTYD</p>
<p>Métricas de Carros Vendidos:</p>
<p>Carros Vendidos YTD</p>
YTD Cars Sold = TOTALYTD(count(car_data[Car_id]), 'Date'[Date])

##### Carros Vendidos MTD
MTD Cars Sold = TOTALMTD(COUNT(car_data[Car_id]), 'Date'[Date])

##### Crescimento Ano a Ano nos Carros Vendidos
YoY Car Sold Growth = [Cars Sold Diff] - [YTD Cars Sold]

##### Diferença entre os Carros Vendidos YTD e os Carros Vendidos PTYD
Sales difference = [YTD Total Sales] -[PYTD Total Sales]

### Parte 2: Requisitos de Gráficos

![image](https://github.com/lagmagalhaes/Projeto-Venda-de-carros/assets/166879716/76054307-800a-4faa-ba10-67e27b9d6b38)

<p>YTD  Vendas Semanal: Exibir um gráfico de linhas ilustrando a tendência semanal das vendas YTD. O eixo X deve representar as semanas, e o eixo Y deve mostrar o valor total das vendas.</p>

<p>Vendas Totais YTD por Estilo de Carro: Visualizar a distribuição das vendas totais YTD entre diferentes estilos de carro usando um gráfico de pizza.</p>

<p>Vendas Totais YTD por Cor: Apresentar a contribuição de várias cores de carros para as vendas totais YTD por meio de um gráfico de pizza.</p>

<p>Carros Vendidos YTD por Região do Revendedor: Mostrar os dados de vendas YTD com base em diferentes regiões de revendedores usando um gráfico de mapa para visualizar a distribuição de vendas geograficamente.</p>

<p>Tendência de Vendas da Empresa em Forma de Grade: Fornecer uma grade tabular que exibe a tendência de vendas para cada empresa. A grade deve mostrar o nome da empresa juntamente com suas cifras de vendas YTD.</p>


