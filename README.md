# Projeto-Venda-de-carros
É uma concessionária de carros que vende diversos modelos de automóveis. 
O objetivo deste projeto é projetar e desenvolver um Dashboard de Vendas de Carros dinâmico e interativo usando o Power BI. Com o Dashboard conseguimos visualizar KPIs críticos relacionados as vendas de carros, ajudando a entender o desempenho das vendas ao longo do tempo e a tomar decisões orientadas por dados.
O Dashboad deve fornecer insights em tempo real sobre os principais indicadores de desempenho (KPIs) relacionados aos nossos dados de vendas. Isso nos permitirá tomar decisões informadas, monitorar o progresso e identificar tendências e oportunidades de crescimento.
## Explicação das funções:
### YTD (Year-to-Date) 
<p>A função YTD em DAX é frequentemente usada para calcular medidas acumuladas ao longo do ano até a data atual.
Em outras palavras, é o total acumulado do ano até ao momento.</p>
<b>Função:TOTALYTD</b>


### MTD (Month-to-Date
<p>Assim como o YTD a função MTD é usada para calcular medidas acumuladas, mas especificamente para o período atual do mês.
Refere-se aos valores acumulados desde o início do mês até a data atual.</p>
<b>Função:TOTALMTD</b>


### YOY (Year-over-Year)
<p>A função YOY em DAX é uma medida que pode ser usada para calcular a variação percentual ou absoluta entre os valores de um determinado período e os valores correspondentes do ano anterior. Por exemplo, se  tivermos dados de vendas mensais, pode usar a função YOY para calcular quanto as vendas deste mês diferem das vendas do mesmo mês no ano passado.
Depois de se ter a métrica do ano atual e anterior,é necessário fazer uma <b>divisão</b> no Power bi.</p>
Como estamos a analisar uma variação entre períodos, o resultado é um percentual %.


### LY (Last Year)
<p>LY em DAX geralmente se refere a "Last Year" (Ano Passado), e é usada para calcular medidas ou valores correspondentes ao mesmo período do ano anterior.</p>
<b>Função:SAMEPERIODLASTYEAR</b>

## Parte 1: Requisitos das Vendas (Medidas)
<p>Vendas Totais do Ano até a Data (YTD) </p>
YTD Total Sales = TOTALYTD(sum(car_data[Price ($)]),'Date'[Date])

<p>Vendas Totais do Mês até a Data (MTD)</p>
MTD Total Sales = TOTALMTD(sum(car_data[Price ($)]),'Date'[Date])

<p>Crescimento Ano a Ano (YOY) nas Vendas Totais</p>
YTD Total Sales = TOTALYTD(sum(car_data[Price ($)]),'Date'[Date])

<p>Diferença entre as Vendas YTD e as Vendas do Ano Anterior até a Data (PTYD)</p>
<p>Primeiro: </p>
<p>PYTD Total Sales = CALCULATE(sum(car_data[Price ($)]), SAMEPERIODLASTYEAR('Date'[Date]))</p>
<p>Segundo:</p>
<p>Sales difference = [YTD Total Sales] -[PYTD Total Sales]</p>

<p>Análise do Preço Médio:</p>
<p> Médio YTD</p>
YTD Cars Sold = TOTALYTD(count(car_data[Car_id]), 'Date'[Date])

<p>Preço Médio MTD</p>
MTD Total Sales = TOTALMTD(sum(car_data[Price ($)]),'Date'[Date])

<p>Crescimento Ano a Ano no Preço Médio</p>
<p>Diferença entre o Preço Médio YTD e o Preço Médio PTYD</p>
<p>Métricas de Carros Vendidos:</p>
<p>Carros Vendidos YTD</p>
YTD Cars Sold = TOTALYTD(count(car_data[Car_id]), 'Date'[Date])

<p>Carros Vendidos MTD</p>
MTD Cars Sold = TOTALMTD(COUNT(car_data[Car_id]), 'Date'[Date])

<p>Crescimento Ano a Ano nos Carros Vendidos</p>
YoY Car Sold Growth = [Cars Sold Diff] - [YTD Cars Sold]

<p>Diferença entre os Carros Vendidos YTD e os Carros Vendidos PTYD</p>
Sales difference = [YTD Total Sales] -[PYTD Total Sales]

#### Parte 2: Requisitos de Gráficos

![image](https://github.com/lagmagalhaes/Projeto-Venda-de-carros/assets/166879716/76054307-800a-4faa-ba10-67e27b9d6b38)


