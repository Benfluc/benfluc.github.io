# PREVISÃO DO VALOR DE EXPORTAÇÃO DO CAFÉ ARÁBICA COM MODELOS DE INTELIGÊNCIA ARTIFICIAL: UM ESTUDO COMPARATIVO ENTRE REDES NEURAIS E ÁRVORES DE DECISÃO
 
## Resumo
O Brasil é o maior produtor e exportador de café do mundo, e o valor obtido com essas exportações tem impacto direto na economia nacional. Prever o preço mensal do café arábica representa uma ferramenta estratégica para produtores, exportadores e formuladores de políticas públicas. Este estudo comparou cinco modelos de aprendizado de máquina aplicados à previsão do valor mensal do café arábica, com base em dados históricos do CEPEA de janeiro de 1997 a maio de 2025. Os modelos avaliados foram: Multilayer Perceptron (MLP), Long Short-Term Memory (LSTM), Gated Recurrent Unit (GRU), Random Forest e XGBoost. As redes neurais MLP e GRU apresentaram os melhores desempenhos, com R² superiores a 0,96 e baixos erros percentuais (MAPE < 6,3%), superando significativamente os modelos baseados em árvores de decisão. Os resultados indicam que redes neurais são mais adequadas para a modelagem de séries temporais financeiras no contexto do agronegócio brasileiro. 

## Tecnologias
Python, Pandas, Scikit-learn, TensorFlow, MatLab.

## Resultados
- R² > 0.9691 (MLP, LSTM, GRU)
- MAPE inferior a 6%
- Comparativo crítico entre Redes Neurais e Árvores de Decisão


## Link para o artigo
[Ver artigo completo](https://medium.com/@luciojuniobenfica2/forecasting-coffee-export-values-using-artificial-intelligence-a-comparative-study-between-neural-f2ff56e32114)

## Códigos
- [MLP](Preço_café_MLP.ipynb)
- [GRU e LSTM](Preço_café_GRU_LSTM.ipynb)
- [Árvores de Decisão](Preço_café_XGBoost_RANDOM.ipynb)
