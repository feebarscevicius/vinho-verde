# Vinho Verde

Teste realizado para a cognitivo.ai, com o objetivo de criar um modelo para estimar a qualidade do vinho, com base em de vinhos portugueses "Vinho Verde", que possuem variantes de vinho branco e tinto. Devido a questões de privacidade, apenas variáveis físico-químicas (input) e sensoriais (output) estão disponíveis (por exemplo, não há dados sobre tipo de uva, marca do vinho, preço de venda, etc).

## Instruções

A análise exploratória está no notebook **01_eda.ipynb** e o modelo está em **02_model.ipynb**. O arquivo **utils.py** contém funções auxiliares usadas na exploratória e na modelagem. As bibliotecas utilizadas estão listadas no **requirements.txt**

## Como foi a definição da sua estratégia de modelagem?

A estratégia foi baseada no tipo de problema (aprendizado supervisionado) e nas características dos preditores e resposta presentes na base. Como existe correlação entre preditores, usei um modelo com regularização para evitar que os coeficientes "estourassem", prejudicando a qualidade da predição. E, por se tratar de um problema de regressão onde não haviam dados para toda a amplitude possível da resposta, considerei que um modelo linear seria a melhor opção pois é possível extrapolar a reta ajustada para prever valores que não foram observados no treino.

## Como foi definida a função de custo utilizada?

A função de custo não precisou ser definida, pois é parte do modelo *Elastic Net*, não podendo ser escolhida / customizada:

![](assets/elastic.png)

## Qual foi o critério utilizado na seleção do modelo final? 

## Qual foi o critério utilizado para validação do modelo? Por que escolheu utilizar este método?

## Quais evidências você possui de que seu modelo é suficientemente bom?