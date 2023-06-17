# Saidas da ETL

O diretório `OUTPUT` contém todos os arquivos gerados pelo processamento ETL. Todos os arquivos são de extensão `csv`.

Todos os arquivos gerados são temporários exceto o arquivo [600Pivot_Flat.csv](https://github.com/LabPEC/ProjetoAnaliseDados/blob/main/02Explorar/INPUT/600Pivot_Flat.csv).

Os arquivos temporários servem para acompanhamento da evolução do processamento das bases originais até produzir um arquivo contendo uma tabela cujas linhas contêm os bairros da Grande Vitória (mapeadas para os códigos de bairros do IBGE) e cujas colunas contêm as atividades econômicas exercidas nesses bairros (atividades também presentes no CNAE).

Cada célula da tabela de saida contém a quantidade daquela atividade (coluna) naquele bairro (linha). O arquivo de saida servirá de entrada para o próximo módulo (bloco de notas) de [Exploração dos Dados](https://github.com/LabPEC/ProjetoAnaliseDados/tree/main/02Explorar).

Os arquivos de saida não aparessem aqui no repositório. Para enxergá-los é necessário rodar o programa em sua maquína.


