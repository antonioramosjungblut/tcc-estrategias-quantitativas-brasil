# tcc-estrategias-quantitativas-brasil
Código, scripts e data-sets utilizados no TCC que investigou estratégias quantitativas de investimento no mercado acionário brasileiro.





Introdução dos códigos deste GITHUB.

Para rodagens dos códigos temos 3 data-sets base: 
*O Primeiro refere-se as planilhas com os indicadores já calculados de cada empresa, filtradas pelo seu valor de liquidez diária mínimo e empresas válidas que estavam sendo negociadas no período da análise.  
-aqui teremos 1 data-set para cada período para rodar as estratégias da Magic-Formula normal. Os data-sets tem os nomes de "1996" para classificações formadas em 01/04/1996 até "2024" para classificações formadas dia 01/04/2024 
-e também teremos 1 data-set para rodar as estratégias da Magic-Formula que usarão otimização dos pesos dos ativos (visto que na otimização dos ativos utilizamos modelo de média-variância de Markowitz com os cálculos de 3 anos para trás, assim só entrou nesse data-set empresas que estavam sendo negociadas ao menos 3 anos na bolsa no período, enquanto n data-set normal as empresas precisavam apenas estarem sendo negociadas no período de análise). Esse data-set vai ser só 1 em que cada aba terá um ano de formação das classificações e o nome do arquivo é "data-set-base-estrategias-com-otimMarkowitz" 
*O segundo data-set refere-se a uma planilha contendo os preços diários de todos os ativos negociados em todo o período. Esse data-set não foi possível incluir visto que passava e muito do limite máximo de tamanho do arquivo.
*O terceiro data-set refere-se aos preços dos benchmarks utilizados na análise. Esse data-set chama-se "dados-valores-dos-indices"


A partir dai conseguimos rodar todos os códigos para obter os resultados e os códigos foram rodados da seguinte maneira:
*primeiro era rodado um código para definir a classificação das empresas dentro de cada estratégia da Magic Formula. (esses códigos tem nome: "Código MFX + indicadores da estratégia);
*após isso era rodado um código para criar um data-set com os preços diários apenas do universo de empresas que foram classificadas dentro de cada estratégia apenas no período necessário para analisar os resultados. (esses códigos tem nome: "código_precos_MFX");
*após isso era rodado um código sobre esse data-set dos preços diários que calcula estatísticas de resultados como retornos, desvio-padrão, etc. (esses códigos tem nome: "códigos_indices_resultados_MFX");
*após isso era rodado um código que compilava todos os resultados de cada estratégia e cada carteira em uma só planilha para que pudesse ser feita uma melhor análise. (esse código tem nome: "códigos_resultados_retornos_geral").
***OBS - em algumas estratégias os 3 códigos estão todos juntos.


Rodando eles conseguimos gerar todas as classificações, data-sets de preços e resultados de cada estratégia.
-as classificações são os arquivos com nome "MFX_empresas";
-os data-sets de preços para cada ano em cada estratégia tem o nome de "precos_empresas_MFX";
-os resultados de cada carteira em cada ano de cada estratégia tem o nome de "indices_resultados_MFX";
***OBS - nas estratégias com otimizacao via Markowitz ainda temos os arquivos com os pesos de cada ativo de cada estratégia e o nome do arquivo é "pesos_empresas_MFX";
-após isso foi rodado o código para compilar todos os resultados e a planilha obtida chama-se "retornos_resultados".
