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

## Parte 1: Requisitos das Vendas (Medidas)
#### Vendas Totais do Ano até a Data (YTD) 
![image](https://github.com/lagmagalhaes/Projeto-Venda-de-carros-PBI/assets/166879716/0ff8e0cf-08c7-4f2c-9974-eb2b42057541)



#### Vendas Totais do Mês até a Data (MTD)
![image](https://github.com/lagmagalhaes/Projeto-Venda-de-carros-PBI/assets/166879716/5031914a-2103-4d0f-9908-428d7b1c7b3b)


#### Crescimento Ano a Ano (YOY) nas Vendas Totais
![image](https://github.com/lagmagalhaes/Projeto-Venda-de-carros-PBI/assets/166879716/757deb84-13f1-4b74-8259-9aa830768ff6)



#### Diferença entre as Vendas YTD e as Vendas do Ano Anterior até a Data (PTYD)
**Primeiro:**
![image](https://github.com/lagmagalhaes/Projeto-Venda-de-carros-PBI/assets/166879716/fb30eacf-1e24-44ad-8b43-baf24a87b433)

**Segundo:**
![image](https://github.com/lagmagalhaes/Projeto-Venda-de-carros-PBI/assets/166879716/76de226c-5ba9-4bfd-89a0-57ae5a10bafc)


### Análise do Preço Médio:
#### Médio YTD
![image](https://github.com/lagmagalhaes/Projeto-Venda-de-carros-PBI/assets/166879716/4026b75d-97e6-48e4-9262-950ce63768c3)

#### Preço Médio MTD
![image](https://github.com/lagmagalhaes/Projeto-Venda-de-carros-PBI/assets/166879716/5ed350f4-dfc9-4b75-8978-adf0361cccfd)


#### Crescimento Ano a Ano no Preço Médio
<p>Diferença entre o Preço Médio YTD e o Preço Médio PTYD</p>
<p>Métricas de Carros Vendidos:</p>
<p>Carros Vendidos YTD</p>
![image](https://github.com/lagmagalhaes/Projeto-Venda-de-carros-PBI/assets/166879716/0a71d482-7ee1-4441-89e7-3534206e6b61)


#### Carros Vendidos MTD
![image](https://github.com/lagmagalhaes/Projeto-Venda-de-carros-PBI/assets/166879716/9a125570-1560-4385-bd8a-a75b7ad16d9c)


#### Crescimento Ano a Ano nos Carros Vendidos
![image](https://github.com/lagmagalhaes/Projeto-Venda-de-carros-PBI/assets/166879716/3b3c7ec9-2db5-4abf-b923-10b78ea4e367)

#### Diferença entre os Carros Vendidos YTD e os Carros Vendidos PTYD
![image](https://github.com/lagmagalhaes/Projeto-Venda-de-carros-PBI/assets/166879716/41ad1322-3279-4936-abb0-bda96824d7c5)


## Parte 2: Requisitos de Gráficos

![image](https://github.com/lagmagalhaes/Projeto-Venda-de-carros/assets/166879716/76054307-800a-4faa-ba10-67e27b9d6b38)

<p>YTD  Vendas Semanal: Exibir um gráfico de linhas ilustrando a tendência semanal das vendas YTD. O eixo X deve representar as semanas, e o eixo Y deve mostrar o valor total das vendas.</p>

<p>Vendas Totais YTD por Estilo de Carro: Visualizar a distribuição das vendas totais YTD entre diferentes estilos de carro usando um gráfico de pizza.</p>

<p>Vendas Totais YTD por Cor: Apresentar a contribuição de várias cores de carros para as vendas totais YTD por meio de um gráfico de pizza.</p>

<p>Carros Vendidos YTD por Região do Revendedor: Mostrar os dados de vendas YTD com base em diferentes regiões de revendedores usando um gráfico de mapa para visualizar a distribuição de vendas geograficamente.</p>

<p>Tendência de Vendas da Empresa em Forma de Grade: Fornecer uma grade tabular que exibe a tendência de vendas para cada empresa. A grade deve mostrar o nome da empresa juntamente com suas cifras de vendas YTD.</p>


