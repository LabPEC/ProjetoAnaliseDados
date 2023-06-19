# Saidas da ETL

O diretório `OUTPUT` contém todos os arquivos gerados pelo processamento ETL. Todos os arquivos são de extensão `csv`.

Todos os arquivos gerados são temporários exceto o arquivo [600Pivot_Flat.csv](https://github.com/LabPEC/ProjetoAnaliseDados/blob/main/02Explorar/INPUT/600Pivot_Flat.csv).

Os arquivos temporários servem para acompanhamento da evolução do processamento das bases originais até produzir um arquivo contendo uma tabela cujas linhas contêm os bairros da Grande Vitória (mapeadas para os códigos de bairros do IBGE) e cujas colunas contêm as atividades econômicas exercidas nesses bairros (mapeadas para os códigos de atividades do CNAE agrupados por DIVISÃO).

A definição CNAE para atividades econômicas segue uma estrutura hierárquica de códigos (SEÇÕES, DIVISÕES, GRUPOS, CLASSES E SUBCLASSES) e suas denominações. No arquivo de entrada de atividades nos bairros do Espírito Santo ([ATIVECO_ES](https://github.com/LabPEC/ProjetoAnaliseDados/blob/main/01ETL/INPUT/AtividadesEconomicas_ES.csv.tar.gz)) aparecem apenas a denominação das atividades. Após o processamento, as atividades estão agrupadas pelo código de DIVISÕES, por exemplo, a DIVISÃO "Comércio Varejista" tem código 47 (ver [600Pivot_Flat.csv](https://github.com/LabPEC/ProjetoAnaliseDados/blob/main/02Explorar/INPUT/600Pivot_Flat.csv)).

Cada célula da tabela de saida contém a quantidade daquela atividade (coluna) naquele bairro (linha). , por exemplo, a DIVISÃO "Comércio Varejista" tem código 47 e parece 128 vezes no bairro Alto Lage (que tem código IBGE 3201308049) do município de Cariacica (ver [600Pivot_Flat.csv](https://github.com/LabPEC/ProjetoAnaliseDados/blob/main/02Explorar/INPUT/600Pivot_Flat.csv)). 

O arquivo de saida servirá de entrada para o próximo módulo (bloco de notas) de [Exploração dos Dados](https://github.com/LabPEC/ProjetoAnaliseDados/tree/main/02Explorar).

Os arquivos de saida não aparecem aqui no repositório. Para enxergá-los é necessário rodar em sua máquína (ver [as instruções detalhadas de instalação](https://github.com/LabPEC/ProjetoAnaliseDados/blob/main/INSTALL.md)) o bloco de notas Jupyter [PreparacaoDados.ipynb](https://github.com/LabPEC/ProjetoAnaliseDados/blob/main/01ETL/PreparacaoDados.ipynb) com as [entradas](https://github.com/LabPEC/ProjetoAnaliseDados/tree/main/01ETL/INPUT).


