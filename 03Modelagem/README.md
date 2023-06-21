# Modelagem

O bloco de notas Jupyter [Modelagem.ipynb](https://github.com/LabPEC/ProjetoAnaliseDados/blob/main/03Modelagem/Modelagem12.ipynb) contém todo o código usado para processamento da modelagem dos dados agrupados para criação e testes de um modelo de classificação.

Este bloco de notas recebe como entrada o arquivo construído e fornecido pelo bloco de notas usado para análise exploratória e agrupamento (*clustering*) dos bairros e suas atividades.
O arquivo de entrada contém uma tabela cujas linhas contêm os bairros presentes no arquivo ATIVECO_ES (mapeadas para os códigos de bairros do IBGE) e cuja coluna `pred` contêm a identificação do cluster ao qual cada bairro pertence.

Para a modelagem são utilizados modelos de classificação multiclasse denominados classificadores multiclasses (também chamados classificadores multinomiais). Para análises e comparações foram utilizados os classificadores Stochastic Gradiente Descendente (*Stochastic Gradient Descent* - SGD), $k$-vizinhos mais pŕoximos (*$k$-Nearest Neighbors* - KNN), Florestas Aleatórias (*Random Forest* - RF) e Máquinas de Vetores de Suporte (*Suport Vector Machine* - SVM).

Os modelos foram treinados e avaliados utilizanado o recurso da validação cruzada do Scikit-Learn. Os hiperparâmetros dos modelos foram ajustados utilizanado o recurso de *Grid Search* combinado com validação cruzada do Scikit-Learn.
[//]: # (This may be the most platform independent comment)

