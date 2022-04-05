# Projeto Airbnb Rio - Ferramenta de Previsão de Preço de Imóvel para pessoas comuns 
---------------------------------------
O Airbnb é uma plataforma para alugar acomodaões por temporadas e promover experências únicas. Você pode ser um anfitrião ou um viajante em qualquer lugar do mundo.

No Airbnb, qualquer pessoa que tenha um quarto ou um imóvel de qualquer tipo (apartamento, casa, chalé, pousada, etc.) pode ofertar o seu imóvel para ser alugado por diária. Você cria o seu perfil de host (pessoa que disponibiliza um imóvel para aluguel por diária) e cria o anúncio do seu imóvel.

Nesse anúncio, o host deve descrever as características do imóvel da forma mais completa possível, de forma a ajudar os locadores/viajantes a escolherem o melhor imóvel para eles (e de forma a tornar o seu anúncio mais atrativo)

Existem dezenas de personalizações possíveis no seu anúncio, desde quantidade mínima de diária, preço, quantidade de quartos, até regras de cancelamento, taxa extra para hóspedes extras, exigência de verificação de identidade do locador, etc.

As bases de dados foram retiradas do site kaggle: https://www.kaggle.com/allanbruno/airbnb-rio-de-janeiro

## Problema de Negócio
-----------------------------------------

O desafio é ajudar os anfitriões, sendo eles pessoas comuns da plataforma, a determinar o melhor preço para o seu imóvel com base nas características dele.
Quanto melhor o valor determinado, maior será o ganho do anfitrião garantindo um preço justo e sem problemas de vacância.

Para o viajante também terá consequências relevantes, uma vez que pagará um preço adequado para sua estadia.

## Objetivo 
-----------------------------------------


Construir um modelo de previsão de preço que permita uma pessoa comum que possui um imóvel possa saber quanto deve cobrar pela diária do seu imóvel.

Ou ainda, para o locador comum, dado o imóvel que ele está buscando, ajudar a saber se aquele imóvel está com preço atrativo (abaixo da média para imóveis com as mesmas características) ou não.

## Estratégia de Solução 
-----------------------------------------

**1**. Coletar os dados e consolidar dataset;

**2**. Filtrar atributos/colunas;

**3**. Tratar valores faltantes;

**4**. Checar e modificar a tipagem das variáveis;

**5**. Análise Exploratória de Dados;
   - Checar disposição dos dados
   - Verificar e tratar outliers
   - Eliminar colunas incoerentes ou não condizentes com o objetivo
   - Agrupar valores pulverizados em variáveis categóricas
   - Visualização de mapa baseado na localização dos imóveis
    
**6**. Encoding;
   - Variáveis booleanas True/False em valores 1/0
   - Variáveis categórias pelo método One-Hot-Encoding
    
**7**. Modelo de Predição;
   - Selecionar melhor modelo entre:
        - RandomForestRegressor
        - LinearRegression
        - ExtraTreesRegressor
    
**8**. Aprimoramento do modelo escolhido;
   - Checar importância de cada variável
   - Testar modelo sem atributos pouco relevantes

**9**. Deploy do projeto;
   - Criar um arquivo para o modelo (joblib)
   - Criar um aplicativo na web utilizando Streamlit
