# Saidas do Processamento e Análise Exploratória

O diretório `OUTPUT` contém todos os arquivos gerados pelo Processamento e Análise Exploratória. No diretório [raiz](https://github.com/LabPEC/ProjetoAnaliseDados/tree/main/02Explorar/OUTPUT) estão todos os arquivos de extensão `csv`. No diretório [Imagens](https://github.com/LabPEC/ProjetoAnaliseDados/tree/main/02Explorar/OUTPUT/Imagens) estão todos os arquivos de extensão `png`.

Todos os arquivos gerados são temporários exceto o arquivo [504_PCA_Cluster3.csv](https://github.com/LabPEC/ProjetoAnaliseDados/blob/main/03Modelagem/INPUT/504_PCA_Cluster3.csv).

Os arquivos temporários servem para acompanhamento da evolução do processamento das bases originais até produzir um arquivo contendo uma tabela cujas linhas contêm os bairros da Grande Vitória (mapeadas para os códigos de bairros do IBGE) e cujas colunas contêm um número de *cluster* associado a cada bairro. A tabela possui uma coluna denominada "pred" com a identificação (número inteiro) do cluster ao qual cada linha (bairro) foi atribuído. Por exemplo, o bairro Alto Lage (que tem código IBGE 3201308049) do município de Cariacica pertence ao cluster de número $2$. 

O arquivo de saida servirá de entrada para o próximo módulo (bloco de notas) de [Modelagem](https://github.com/LabPEC/ProjetoAnaliseDados/tree/main/03Modelagem).

Os arquivos de saida não aparecem aqui no repositório. Para enxergá-los é necessário rodar em sua máquína (ver [as instruções detalhadas de instalação](https://github.com/LabPEC/ProjetoAnaliseDados/blob/main/INSTALL.md)) o bloco de notas Jupyter [Processamento_AnaliseExploratoria.ipynb](https://github.com/LabPEC/ProjetoAnaliseDados/blob/main/02Explorar/Processamento_AnaliseExploratoria.ipynb) com as [entradas](https://github.com/LabPEC/ProjetoAnaliseDados/tree/main/02Explorar/INPUT).


