# PREVISÃO DO VALOR DE EXPORTAÇÃO DO CAFÉ ARÁBICA COM MODELOS DE INTELIGÊNCIA ARTIFICIAL: UM ESTUDO COMPARATIVO ENTRE REDES NEURAIS E ÁRVORES DE DECISÃO
 
Abstract. O Brasil é o maior produtor e exportador de café do mundo, e o valor obtido com essas exportações tem impacto direto na economia nacional. Prever o preço mensal do café arábica representa uma ferramenta estratégica para produtores, exportadores e formuladores de políticas públicas. Este estudo comparou cinco modelos de aprendizado de máquina aplicados à previsão do valor mensal do café arábica, com base em dados históricos do CEPEA de janeiro de 1997 a maio de 2025. Os modelos avaliados foram: Multilayer Perceptron (MLP), Long Short-Term Memory (LSTM), Gated Recurrent Unit (GRU), Random Forest e XGBoost. As redes neurais MLP e GRU apresentaram os melhores desempenhos, com R² superiores a 0,96 e baixos erros percentuais (MAPE < 6,3%), superando significativamente os modelos baseados em árvores de decisão. Os resultados indicam que redes neurais são mais adequadas para a modelagem de séries temporais financeiras no contexto do agronegócio brasileiro. 
Keywords: Café; Preço; Séries Temporais; Inteligência Artificial; Redes Neurais
## 1.	INTRODUÇÃO

O Brasil ocupa uma posição de destaque no cenário agrícola mundial, sendo historicamente o maior produtor e exportador de café do planeta. A cultura cafeeira possui profunda relevância econômica, social e histórica para o país, influenciando desde a organização territorial até as relações comerciais internacionais. De acordo com o Conselho dos Exportadores de Café do Brasil (Cecafé), apenas em 2023, as exportações brasileiras de café movimentaram mais de 6 bilhões de dólares, demonstrando o peso dessa commoditie na balança comercial e no Produto Interno Bruto (PIB) nacional. Conforme pode ser visualizado na Fig. 1 o café é produzido em larga escala em todo o território nacional, com destaque para os estados de Minas Gerais e São Paulo, onde grande parte dessa produção é destinada as exportações. 
Além do volume exportado, o valor de exportação em dólares representa um fator-chave para o planejamento estratégico de produtores, exportadores, cooperativas, formuladores de políticas públicas e investidores do setor. Variações nos preços internacionais do café — influenciadas por condições climáticas, flutuações cambiais, oferta global e demanda — podem gerar impactos significativos em toda a cadeia produtiva. Por isso, a previsão acurada dos preços de exportação torna-se uma ferramenta essencial para antecipar riscos, otimizar lucros e garantir maior estabilidade econômica para os agentes envolvidos.

 
Figura 1 – Produção de café no Brasil (IBGE, 2025)

Nos últimos anos, a Inteligência Artificial (IA) tem se consolidado como uma aliada poderosa no campo da análise preditiva, sobretudo no contexto de séries temporais. Modelos como as Redes Neurais Recorrentes (RNN), com destaque para suas variantes Long Short-Term Memory (LSTM) e Gated Recurrent Unit (GRU), demonstram elevada capacidade de capturar padrões sazonais e dependências de longo prazo em séries temporais financeiras e agrícolas. Paralelamente, arquiteturas mais simples como a Multilayer Perceptron (MLP) ainda apresentam bons resultados em determinadas configurações.
Além das redes neurais, algoritmos de aprendizado de máquina como o XGBoost (Extreme Gradient Boosting) e o Random Forest têm sido amplamente utilizados por sua robustez, capacidade de lidar com dados não lineares e desempenho competitivo em diferentes contextos de previsão. Esses modelos possibilitam explorar relações complexas entre variáveis de entrada (como clima, produção, câmbio) e o valor de exportação, sendo, portanto, alternativas eficazes para apoiar decisões estratégicas no setor cafeeiro. Portanto, este artigo tem como objetivo investigar e comparar o desempenho desses modelos de IA na previsão do valor de exportação mensal do café brasileiro, oferecendo uma análise técnica de suas capacidades preditivas e destacando o potencial de aplicação prática para stakeholders da cadeia do agronegócio. O artigo foi dividido da seguinte maneira: no capítulo 2 abordamos os materiais e métodos empregados, bem como as configurações adotadas em cada rede, no capítulo 3 apresentamos e discutimos os resultados obtidos e por fim, no capítulo 4 são expostas as considerações finais.

## 2.	MATERIAIS E MÉTODOS

Os dados utilizados neste estudo foram obtidos a partir do Centro de Estudos Avançados em Economia Aplicada (CEPEA/ESALQ-USP). O conjunto de dados compreende os valores mensais do preço do café arábica em dólares por saca de 60 kg, no mercado brasileiro, abrangendo o período de janeiro de 1997 a maio de 2025. Esta série temporal, composta por 341 observações, reflete a evolução dos preços ao longo do tempo e serve como base para a tarefa de previsão.
A preparação dos dados incluiu a normalização por meio da técnica de MinMaxScaler e a construção de janelas temporais com defasagens (lags) iguais a 6 para permitir que os modelos aprendessem padrões históricos e tendências. A série foi dividida em conjuntos de treinamento (70%) e teste (30%), mantendo a ordem temporal para preservar a integridade da estrutura sequencial dos dados.
Os experimentos foram conduzidos em ambiente Jupyter Notebook, utilizando Python 3.10 como linguagem principal. Para o desenvolvimento e avaliação dos modelos, foram utilizadas as bibliotecas: NumPy e Pandas para manipulação e análise de dados; Scikit-learn para os modelos Random Forest Regressor e XGBoost Regressor, bem como para a aplicação de métodos de validação cruzada e métricas de avaliação; TensorFlow e Keras para a construção e treinamento das redes neurais MLP, LSTM e GRU e a biblioteca Matplotlib para a visualização dos resultados e análise gráfica das previsões.
Para otimizar o desempenho de cada modelo, foi realizado um processo de busca de hiper parâmetros, essencial para ajustar corretamente aspectos como número de neurônios, taxa de aprendizado, profundidade das árvores e número de estimadores. Foram utilizadas duas abordagens complementares para tanto: GridSearchCV, que realiza uma busca exaustiva em um espaço pré-definido de combinações de hiper parâmetros e RandomizedSearchCV, que seleciona aleatoriamente combinações dentro de um espaço amostral especificado, permitindo maior eficiência computacional em espaços de busca maiores. Para avaliar o desempenho dos modelos, as métricas consideradas foram o Erro Médio Absoluto (MAE), Erro Percentual Médio Absoluto (MAPE) e o Coeficiente de Determinação (R²).

## 3.	RESULTADOS

A análise dos resultados obtidos com os cinco modelos de aprendizado de máquina revela diferenças significativas em termos de desempenho, precisão e capacidade de generalização. As métricas consideradas — MAE, MAPE e R² — oferecem uma visão abrangente da eficácia de cada abordagem na tarefa de previsão. O modelo MLP apresentou excelente desempenho, com R² de 0,9691 no conjunto de teste, indicando alta capacidade de explicação da variabilidade dos dados. Além disso, o MAPE de 5,55% sugere um erro percentual relativamente baixo, o que é desejável em aplicações comerciais. Na Figura 2 podemos perceber que o modelo previsto pela MLP (linha laranja) ficou muito próximo dos valores reais (linha azul).

 
Figura 2 – Comparativo entre previsões do modelo MLP e preço real

A rede LSTM também obteve resultados bastante satisfatórios, com R² de 0,9673 e MAPE de 6,08%. Apesar de apresentar um erro ligeiramente maior do que o MLP, a LSTM se destaca pela capacidade de modelar dependências temporais mais longas, o que pode ser útil em cenários com maior variabilidade ou ruído nos dados. A arquitetura GRU, por sua vez, obteve o melhor desempenho entre as redes neurais, com R² de 0,9699, superando ligeiramente o MLP e a LSTM. Embora seu MAPE (6,24%) tenha sido um pouco superior ao do MLP, o equilíbrio entre erro absoluto, erro quadrático e coeficiente de determinação evidencia sua robustez. Na Figura 3 podemos ver as previsões feitas pelos modelos LSTM e GRU respectivamente.
 
 
Figura 3 – Comparativo previsões dos modelos LSTM e GRU vs valores reais

Por outro lado, os modelos baseados em árvores — Random Forest e XGBoost — apresentaram desempenho inferior. O Random Forest alcançou um R² de apenas 0,8271, com MAPE de 7,39% e um RMSE bastante elevado (1165,67), indicando maior variabilidade nos erros. O XGBoost teve um leve ganho sobre o Random Forest, atingindo R² de 0,8515, mas com MAPE de 8,12%, o mais alto entre todos os modelos testados. Esses resultados sugerem que, embora robustos, os métodos baseados em árvores podem ter limitações na modelagem de séries temporais altamente dinâmicas como os preços do café. A Tabela 1 traz o comparativo das métricas entre todos os modelos.

Tabela 1 – Comparativo entre os modelos
Modelo	R²	MAE	MAPE (%)
MLP	0,9691	10,14	5,55
LSTM	0,9697	10,92	6,08
GRU	0,9699	10,64	6,24
Random Forest	0,8271	17,12	7,39
XGBoost	0,8515	17,88	8,12

Observa-se, portanto, que as redes neurais, especialmente MLP e GRU, foram as mais eficazes na tarefa de previsão, apresentando melhores métricas em comparação aos modelos baseados em árvores. A simplicidade e a velocidade do MLP, aliadas à alta acurácia da GRU, sugerem que esses modelos são promissores para aplicações práticas no mercado cafeeiro.
						
## 4.	CONSIDERAÇÕES FINAIS 

Os resultados evidenciaram o potencial das redes neurais artificiais, especialmente MLP e GRU, na modelagem de séries temporais financeiras. O modelo MLP destacou-se pela combinação entre alta acurácia e baixo erro percentual, sendo uma alternativa prática e eficaz. A GRU, por sua vez, apresentou o melhor R², reforçando sua capacidade de lidar com padrões temporais complexos. Em contrapartida, os modelos Random Forest e XGBoost apresentaram desempenho inferior, com maiores erros absolutos e percentuais, o que indica menor adequação para o tipo de dado analisado. Embora esses algoritmos sejam amplamente utilizados em tarefas de regressão, seus resultados sugerem limitações quando aplicados diretamente à previsão de séries temporais não estacionárias como os preços do café.
Dessa forma, conclui-se que modelos baseados em redes neurais são ferramentas promissoras para apoiar a tomada de decisão no agronegócio, oferecendo previsões mais precisas que podem beneficiar produtores, exportadores e formuladores de políticas públicas. Trabalhos futuros podem incluir a incorporação de variáveis exógenas (como clima, câmbio e demanda internacional), o uso de redes híbridas e a avaliação em contextos regionais específicos, como os estados produtores do Sudeste brasileiro.

## REFERÊNCIAS

IBGE. Mapa – Café – Valor da produção (mil reais). Disponível em: https://www.ibge.gov.br/explica/producao-agropecuaria/cafe/br. Acesso em: 06 jul. 2025.
CEPEA. Indicador do Café Arábica CEPEA/ESALQ. Disponível em:  https://www.cepea.org.br/br/indicador/cafe.aspx. Acesso em: 06 jul. 2025.
