# InStyle Store

## Descrição da empresa e seu problema
- A loja de moda InStyle é uma grande loja de roupas, mas enfrenta desafios significativos em relação à experiência do cliente. 
- O principal obstáculo para aumentar as receitas de uma loja reside na manutenção da qualidade do produto e na satisfação do cliente. À medida que a empresa expande sua base de clientes, a equipe de produtos encontra dificuldades em identificar as necessidades predominantes dos clientes.

- Em vista disso, a InStyle montou uma equipe com a tarefa de **treinar um algoritmo para classificar os clientes de uma planilha em “Satisfeito” ou “Neutro/Insatisfeito”**, prevendo quais clientes ficarão Insatisfeitos e portanto agindo rápido para entender o motivo da insatisfação e reverter o cenário do cliente. 
- Assim, após a classificação, é possível entrar em contato com os clientes insatisfeitos para oferecer promoções e dar discontos, de maneira que a empresa melhore a sua relação com eles.

## Descrição do Objetivo
- **Gerar insights através dos dados**
- **Produzir informações visuais sobre a base de clientes da empresa**
- **Classificar e identificar os clientes insatisfeitos através de um algoritmo de Machine Learning**

## Solução do Projeto

- **Importações:** importações de bibliotecas e pacotes, definição de configurações, criação de funções e carregamento dos dados;
- **Descrição dos dados:** apresenta-se o dataset, suas dimensões, colunas com descrições, tipos de dados;
- **Pré-processamento e exploração:** renomeia-se colunas, checar a presença de dados faltantes, balanceamento da categoria alvo, descrição das variáveis numéricas e categóricas, heatmap de correlação;
- **Análise Exploratória de Dados (EDA):** nesta seção busca-se responder perguntas sobre o dataset que possam influenciar no entendimento do negócio e na maneira como buscamos pela solução do problema. As principais conclusões da EDA são:
  
  > - A proporção de clientes satisfeitos é menor do que aqueles em dúvida (neutros) e insatisfeitos, mas não é muito menor no geral, pois a relação fica em 45-55%;
  > - A distribuição etária apresenta uma leve assimetria à direita, indicando que a maioria dos clientes tem menos de 40 anos. Por outro lado, a quantidade de clientes satisfeitos é maior do que os neutros/insatisfeitos para as idades entre 39 e 60 anos. Poderíamos inferir que a geração mais jovem é mais difícil de agradar ou que eles não têm uma boa experiência com a loja.
  > - Consumidores que compram algo para si mesmos são muito mais insatisfeitos. Por outro lado, aqueles que compram um presente se contentam mais com a experiência e a loja;
  > - Clientes ficam mais satisfeitos em lojas de tamanho grande.

- **Feature Engineering:** nesta parte realiza-se o *Encoding* de variáveis, divide-se o dataset em treino, teste e validação, imputa-se os dados faltantes (*KNN-Imputer*), realiza-se o *Scaling* de variáveis (MinMaxScaler e RobustScaler) e define-se quais as variáveis são mais importantes para o modelo a seguir;
- **Machine Learning:** os seguintes modelos de ML foram testados e avaliados a partir das métricas: **Acurácia, Precisão, Recall, F1 Score, Classification Report e Matriz de Confusão.**
  - **Logistic Regression, Random Forest, XGBoost, LightGBM;**
  - Por ter performado melhor, o modelo de LightGBM foi escolhido para empregar **Cross-Validation** e **Hyperparameter Tuning**
  - Os resultados de Cross Validation não se mostraram significativamente superiores, mas o modelo melhorou através do Hyperparameter (RandomizerSearchCV);
  - Por fim, o melhor modelo foi empregado nos dados de Validation, mantendo sua performance.

# Conclusões do Projeto
## **Impacto Estratégico da Solução**
A implementação do modelo de Machine Learning para classificar a satisfação do cliente na InStyle marca uma virada estratégica significativa. O foco na satisfação do cliente não apenas aborda desafios cruciais da empresa, mas também redefine a abordagem para aprimorar a experiência do cliente e consolidar sua posição no mercado de moda.

## Benefícios Tangíveis
**1. Elevação da Satisfação do Cliente:**
- Identificar clientes insatisfeitos ou neutros permite à equipe de atendimento abordá-los de maneira personalizada, atendendo às suas preocupações e oferecendo soluções.
- Essa prática não apenas melhora a satisfação do cliente, mas também reduz queixas, contribuindo para aprimorar a reputação da InStyle.

**2. Fidelização e Retenção de Clientes:**
- O modelo de classificação de clientes possibilita ações proativas para resolver as causas de insatisfação, promovendo o retorno desses clientes para futuras compras.
- Fortalecer os laços empresa-cliente não só fideliza consumidores a longo prazo, mas também amplia o valor do ciclo de vida do cliente.

**3. Direcionamento Eficiente de Marketing:**
- O modelo orienta a equipe de marketing na direção certa, concentrando esforços em públicos mais propensos a se tornarem clientes satisfeitos e leais, ou revertendo situações de insatisfação.

**4. Otimização de Custos:**
- A identificação aprimorada de clientes reduz os custos operacionais ao permitir que a empresa entre em contato de maneira mais focada, otimizando o tempo de funcionários de outros setores.

## Avaliação da Precisão do Modelo
- Os resultados alcançados, com uma Precision acima de 87% e F1 Score de 85%, refletem uma implementação bem-sucedida do modelo nos conjuntos de treino-teste e também no de validação.
- Ao considerar os resultados de validação, a abordagem de contatar clientes classificados como "Neutro ou Insatisfeito" mostra uma taxa de erro inferior a 14% na oferta de crédito, descontos ou promoções.

## **Considerações para o Futuro**
Embora o resultado final, com uma taxa de acerto superior a 86%, seja positivo para a empresa, a empresa reconhece o potencial para melhorias contínuas. A obtenção de mais dados, a expansão do poder computacional e um investimento adicional de tempo são cruciais para aprimorar ainda mais o modelo e garantir o aprimoramento das operações.

# Além do Modelo de Machine Learning
É essencial ressaltar que o modelo de Machine Learning não é o fim, mas sim um meio para alcançar o verdadeiro objetivo: a compreensão aprofundada dos clientes e seus comportamentos, especialmente aqueles insatisfeitos. **O foco final é a melhoria contínua do serviço da InStyle, fortalecendo as relações com os clientes e garantindo sua retenção a longo prazo.**

