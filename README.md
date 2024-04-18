# Projeto-Venda-de-carros
É uma concessionária de carros que vende diversos modelos de automóveis. 
O objetivo deste projeto é projetar e desenvolver um Dashboard de Vendas de Carros dinâmico e interativo usando o Power BI. Com o Dashboard conseguimos visualizar KPIs críticos relacionados as vendas de carros, ajudando a entender o desempenho das vendas ao longo do tempo e a tomar decisões orientadas por dados.
O Dashboad deve fornecer insights em tempo real sobre os principais indicadores de desempenho (KPIs) relacionados aos nossos dados de vendas. Isso nos permitirá tomar decisões informadas, monitorar o progresso e identificar tendências e oportunidades de crescimento.
## Visão Geral das Vendas:
### YTD (Year-to-Date) 
<p>A função YTD em DAX é frequentemente usada para calcular medidas acumuladas ao longo do ano até a data atual.
Em outras palavras, é o total acumulado do ano até ao momento.</p>

#### Função:TOTALYTD

### MTD (Month-to-Date
<p>Assim como o YTD a função MTD é usada para calcular medidas acumuladas, mas especificamente para o período atual do mês.
Refere-se aos valores acumulados desde o início do mês até a data atual.</p>

#### Função:TOTALMTD

### YOY (Year-over-Year)
<p>A função YOY em DAX é uma medida que pode ser usada para calcular a variação percentual ou absoluta entre os valores de um determinado período e os valores correspondentes do ano anterior. Por exemplo, se  tivermos dados de vendas mensais, pode usar a função YOY para calcular quanto as vendas deste mês diferem das vendas do mesmo mês no ano passado.
Depois de se ter a métrica do ano atual e anterior,é necessário fazer uma <b>divisão</b> no Power bi.</p>
Como estamos a analisar uma variação entre períodos, o resultado é um percentual %.


### LY (Last Year)
LY em DAX geralmente se refere a "Last Year" (Ano Passado), e é usada para calcular medidas ou valores correspondentes ao mesmo período do ano anterior.
#### Função:SAMEPERIODLASTYEAR
