# Projeto em Ciência e Análise de Dados

Este projeto tem o objetivo de ser um arcabouço de ensino e aprendizagem em Ciência e Análise de Dados utilizando a linguagem de programação Python. Com ele é possível acompanhar e reproduzir de forma prática e explicativa os passos do Ciclo de Análise de Dados, conforme figura abaixo:
<div align="center">
  
![](https://github.com/LabPEC/ProjetoAnaliseDados/blob/main/Docs/CicloDadosBW.png)

  Fonte: próprio autor
  
</div>

O problema aqui tratado consiste em, fornecidas as tabelas de
- Classificação Nacional de Atividades Econômicas do IBGE,
- Bairros utilizados pelo IBGE no Censo Demográfico de 2010 e suas características sócio-econômicas e
- Atividades econômicas desenvolvidas nos bairros do Espírito Santo (anonimizada),

criar um modelo que permita relacionar bairros, atividades econômicas e características sócio-econômicas.

O relacionamento criado entre bairros, atividades econômicas e características sócio-econômicas permitirá uma diversidade de análises como, por exemplo, determinar bairros equivalentes, identificar bairros promissores para exercer uma determinada atividade, entender como as características sócio-econômicas influenciam nas atividades econômicas dos bairros e vice-versa, entre outras.


Após a fase de Coleta de Dados, foi definido durante a fase Exploração e Processamento dos dados que os bairros a serem tratados deveriam pertencer aos municípios da Grande Vitória (GV):
 - Cariacica,
 - Serra,
 - Viana,
 - Vila Velha e
 - Vitória

já que os códigos dos bairros da GV foram definidos pelo IBGE pois seus municípios tiveram suas leis de bairros aprovadas até agosto de 2010. No Espírito Santo somente 12 municípios  tiveram suas leis de bairros aprovadas até agosto de 2010. São eles: Aracruz, Barra de São Francisco, Cachoeiro de Itapemirim, Cariacica,
Colatina, Ecoporanga, Iúna, Linhares, Serra, Viana, Vila Velha e Vitória.

Mais especificamente, o objetivo do modelo de aprendizado de máquina proposto é identificar se a estrutura econômica e o mercado de trabalho dos bairros da Grande Vitória podem ser explicadas pelas variáveis sócio-econômicas do Censo Demográfico de 2010. O Censo Demográfico é uma pesquisa realizada pelo IBGE em todos os domicílios do território nacional, cerca de 58 milhões atualmente. É a principal fonte de dados sobre as características socioeconômicas da população brasileira, refletindo um retrato da nossa sociedade que nos permite saber como somos, onde estamos e como vivemos.

A importância da análise das características das atividades econômicas dos bairros reside no fato de compreender melhor o mercado urbano, fornecendo subsídios para políticas  de planejamento urbano com alocação e incentivo de novas atividades econômicas nos bairros.


Este arcabouço está organizado da seguinte forma:

* Para construir um ambiente para executar os códigos aqui disponibilizados, [leia as instruções detalhadas de instalação](https://github.com/LabPEC/ProjetoAnaliseDados/blob/main/INSTALL.md)
* o diretório [01ETL](https://github.com/LabPEC/ProjetoAnaliseDados/tree/main/01ETL) contém os códigos e arquivos para a execução da fase de Exploração dos Dados (*Extract, Transform and Load* -- ETL)



