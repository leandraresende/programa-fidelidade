## 1 - Problema de negócio

A empresa All in One Place é um e-commerce outlet multimarcas cujo time de Marketing vai lançar um programa de fidelidade para os melhores clientes da base, chamado Insiders. 

O time de dados da empresa precisa determinar quem são os clientes elegíveis para participar do Insiders. E, em posse dessa lista, o time de Marketing fará uma sequência de ações personalizadas e exclusivas ao grupo, de modo a aumentar o faturamento e a frequência de compra.

Como resultado para esse projeto, será entregue uma lista de clientes elegíveis a participar do Insiders e suas características principais, porcentagem de contribuição do faturamento advinda desse grupo, além de informações sobre outros grupos de clientes.

## 2 - Estratégia de solução

A análise foi feita em ciclos e cada ciclo baseou-se no método CRISP-DS com as seguintes etapas: coleta e limpeza dos dados (aplicadas apenas no primeiro ciclo), análise descritiva, filtragem de variáveis, feature engineering, análise exploratória, treinamento dos algoritmos com fine-tuning e avaliação, modelagem dos dados, análise dos grupos gerados. 

A segmentação dos clientes foi 'baseada' no método RFM - uma ferramenta de segmentação de clientes que analisa o comportamento de compra baseado em três critérios: Recência, Frequência e Valor Monetário, onde

Recência (R): o tempo decorrido desde a última compra do cliente.<br>
Frequência (F): medida do número de compras realizadas por um cliente em um período específico.<br>
Valor Monetário (M): o total gasto por um cliente. 

O primeiro ciclo dedica-se, principalmente, à criação dessas três variáveis e suas análises. Posteriormente, é feito o estudo de embeddings e sua avaliação em relação ao dataframe utilizado. A partir desse resultado, há a modelagem dos dados e, consequentemente, a análise da segmentação de criada. O produto final é uma lista dos agrupamentos de clientes e suas características.

No segundo ciclo, são criadas novas variáveis e, similarmente ao que foi feito no primeiro ciclo, análises das mesmas e dos embeddings (para esse novo conjunto de dados), a modelagem dos dados e análise dos clusters. Novamente, o produto final é uma lista segmentada de clientes.

Já no terceiro ciclo, o foco é o estudo dos embeddings e a modelagem dos dados. Nessa etapa, são adicionados mais algoritmos de clusterização para comparação das performances. O produto final é a lista de clientes agrupados por categorias. 

## 3 - Premissas consideradas

Durante as análises dos dados, fui considerado que linhas do dataframe que possuiam quantidades negativas (juntamente ao número do invoice iniciado pela letra C) eram devolução de produtos ou cancelamento de pedido. O preço unitário mínimo considerando foi $0.04. E stock codes indicados por letras ou palavras não foram considerados por não termos informações à respeito de seus significados.

## 4 - Produto final

O produto final é uma lista com clientes elegíveis para participar do programa Insiders bem como suas características médias. Os demais clientes também foram divididos em grupos (clusters) e suas características estão presentes na lista final. Essas informações podem ser usadas pelo time de Marketing e/ou de Vendas para realizar estratégias específicas como bônus, promoções, prêmios que se adequam melhor a cada tipo de cliente. Foram adicionados também a porcentagem e o valor do faturamento correspondente a cada segmento de clientes.

## 5 - Conclusões

O time de Marketing da empresa All in One Place vai lançar um programa de fidelidade para os melhores clientes da base. O objetivo desse projeto era criar uma lista de clientes elegíveis a participar desse programa. O produto final produzido contém a lista de clientes para participar do programa Insiders bem como listas segmentadas com os demais clientes da base de dados. As informações apresentadas também podem ser usadas pelo time de Vendas da empresa.

## 6 - Próximos passos

- Em ciclos sequentes, podem ser adicionadas às análises, informações como país do comprador e descrição dos produtos comprados. 
- Novas variáveis também podem ser criadas tais como tamanho médio da cesta, valor do ticket médio, quantidade de produtos únicos na cesta.
- Incluir novos algoritmos de clusterização na fase de treinamento buscando melhorar a performance da modelagem de dados.
